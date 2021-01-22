<template>
  <div id="nav">
    <p><router-link to="/">sports</router-link> |</p>
    <p><router-link to="/example2">medicine</router-link> |</p>
    <p><router-link to="/example3">home</router-link></p>
  
  <router-view :key="$route.fullPath"/>
  </div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align:right;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #ebeff3;
}

#nav a.router-link-exact-active {
  color: #ffffff;
}
</style>
