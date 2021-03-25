<template>
  <div id="nav">
    <div class="conteinerNav">
      <div class="routerHome">
        <router-link to="/">CleanArchitecture.WebUI_vue</router-link>
      </div>
      <div class="links">
        <router-link to="/">Home</router-link> 
        <router-link to="/Counter">Counter</router-link>
        <router-link to="/FetchData">Fetch data</router-link>
      </div>      
    </div>    
  </div>
  <router-view /> 
</template>

<style>
body{
  margin: 0px;
}
#app {
  font-family: -apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,"Helvetica Neue",Arial,"Noto Sans",sans-serif,"Apple Color Emoji","Segoe UI Emoji","Segoe UI Symbol","Noto Color Emoji";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: rgb(33, 37, 41); /* #2c3e50;*/
}

#nav {
  width: 100%;
  box-shadow: 0 0.25rem 0.75rem rgb(0 0 0 / 5%);
  border-bottom: 1px solid #dee2e6;
}
.conteinerNav, .conteiner{
  padding: 0.5rem 5% 1rem 5%;

}
.links a{
  padding: 0 10px;
}

#nav div a {
  color: rgba(0,0,0,.9);  
}
.routerHome {   font-size: 1.25rem; }
#nav .conteinerNav div {
  display: inline;
}

#nav .links a.router-link-exact-active {
  color: #42b983;
}
.links{
  float: right;
}
.btn-primary {
  color: #fff;
  background-color: #1b6ec2;
  border-color: #1861ac;
}

</style>
