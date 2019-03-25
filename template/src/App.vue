<template>
  <div id="app">
    {{#router}}
    <router-view/>
    {{else}}
    <Home/>
    {{/router}}
  </div>
</template>

<script>
{{#unless router}}
import Home from './page/home'

{{/unless}}
export default {
  name: 'App'{{#router}}{{else}},
  components: {
    Home
  }{{/router}}
}
</script>

<style>
* {
  margin: 0;
}

body, html {
  height: 100%;
}

#app {
  margin-top: 60px;
  color: #2c3e50;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
}
</style>
