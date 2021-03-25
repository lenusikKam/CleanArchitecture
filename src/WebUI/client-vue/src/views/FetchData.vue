<template>
  <div class="conteiner">
    <h1 id="tableLabel">Weather forecast</h1>

    <p>This component demonstrates fetching data from the server.</p>

    <p v-if="!forecasts && !errors"><em>Loading...</em></p>

    <div v-if="errors">
      <div  v-for="error in errors" v-bind:key="error" > 
        There was an error: {{ error.message }}  
      </div>
    </div>

    <table
      class="table table-striped"
      v-if="forecasts"
    >
      <thead>
        <tr>
          <th>Date</th>
          <th>Temp. (C)</th>
          <th>Temp. (F)</th>
          <th>Summary</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="forecast in forecasts" v-bind:key="forecast">
          <td>{{ forecast.date }}</td>
          <td>{{ forecast.temperatureC }}</td>
          <td>{{ forecast.temperatureF }}</td>
          <td>{{ forecast.summary }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      forecasts: null,
      errors: []
    };
  },
  mounted() {
    axios.get("/api/WeatherForecast")
      .then((response) => (this.forecasts = response.data))
      .catch(e=>{ this.errors.push(e) });
  },
};
</script>
