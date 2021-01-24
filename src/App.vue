<template>
  <div id="nav">
    <router-link to="/">Home</router-link> | 
    <router-link to="/example2">Purpose</router-link> |
    <router-link to="/example3">Concept</router-link> |
    <router-link to="/example4">Classes</router-link> |
    <router-link to="/example5">Products</router-link>

  
  <router-view :key="$route.fullPath"/>
  </div>
</template>

<style>
body{
  margin:0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  top: 0px;
  text-align:right;
  font-size:25px;
  color: #2c3e50;
}

#nav {
  position:relative;
  padding:0;
  z-index: 999;
  background-color:black;
}

#nav a {
  font-weight: bold;
  color: #ebeff3;
  z-index: 99;
  top:0px;
}

#nav a.router-link-exact-active {
  top:0px;
  color: #ffffff;
  z-index: 99;
}
</style>
