<template>
  <div id="app">
    <pre>{{ debug(myObj) }}</pre>
  </div>
</template>

<script>
export default {
  mixins: [debug],
  data() {
    return {
      myObj: {
        some: "data",
        other: "values",
      },
    };
  },
  created() {
    console.log(this.debug(this.myObj));
  },
  name: "App",
  components: {},
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
