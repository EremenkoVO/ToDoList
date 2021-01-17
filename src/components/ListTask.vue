<template>
  <div class="container">
    <ul>
      <li v-for="(item, index) in listTask" :key="index" v-text="item"></li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ListTask",
  props: {
    listTask: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style></style>
