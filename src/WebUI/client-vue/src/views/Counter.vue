<template>
  <div class="conteiner">
    <h1>Counter</h1>

    <p>This is a simple example of an Vue.</p>

    <p>Current count: <strong>{{ currentCount }}</strong></p>

    <button class="btn btn-primary" v-on:click="currentCount++;">Increment</button>
  </div>
</template>


<script>
export default {
  data() {
    return {currentCount:0}
  },
}
</script>



