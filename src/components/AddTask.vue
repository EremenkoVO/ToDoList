<template>
  <div class="container">
    <div class="form-group">
      <input
        type="text"
        class="search-input"
        placeholder="Введите текст задачи"
        v-model="taskText"
      />
      <button type="submit" class="btn btn-primary" @click="addTask">
        Добавить
      </button>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    listTask: {
      type: Array,
      default: () => [],
    },
  },
  name: "AddTask",
  data: () => ({
    taskText: "",
  }),
  methods: {
    addTask() {
      this.listTask.push(this.taskText);
    },
  },
};
</script>

<style></style>
