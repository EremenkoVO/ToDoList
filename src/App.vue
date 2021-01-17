<template>
  <div id="app">
    <add-task :list-task="listTask" />
    <hr width="300px" />
    <list-task :list-task="listTask" />
  </div>
</template>

<script>
export default {
  name: "App",
  components: {
    ListTask: () =>
      import(/** webpackChunkName "ListTask" */ "./components/ListTask"),
    AddTask: () =>
      import(/** webpackChunkName "AddTask" */ "./components/AddTask"),
  },
  data: () => ({
    listTask: [],
  }),
};
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
