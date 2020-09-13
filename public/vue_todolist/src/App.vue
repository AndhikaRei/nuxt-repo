<template>
  <div id="app">
    <HeaderComponent/>
    <router-view/>
  </div>
</template>

<script>
import HeaderComponent from "./components/HeaderComponent";
export default {
  name : "app",
  components : {
    HeaderComponent
  }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 10px;
}

#nav a {
  font-weight: bold;
  color: #ffffff;
}

#nav a.router-link-exact-active {
  color: #2c3e50;
}
</style>
