<template>
  <div id="app">
    <NavigationComponent />
    <router-view :key="$route.path" />
  </div>
</template>

<script>
import NavigationComponent from "@/components/NavigationComponent";
export default {
  components: {
    NavigationComponent
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
