<template>
  <div id="app">
    <h4 class="bg-primary text-white text-center p-2">
      ToDo List 1
    </h4>
  </div>
</template>

<script>
export default {
  name: 'App',
  methods: {
    add: function(a,b) {
      var result = a + b;
      return result;
    }
  },
  mounted: function() {
    console.log(this.add(1,3));
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
  margin-top: 60px;
}
</style>
