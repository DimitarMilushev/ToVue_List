<template>
  <div class="list-container">
    <h1>{{ title }}</h1>
    <ul class="task-list">
      <li v-for="task in tasks" :key="task.id">
        <Task
          :title="task.title"
          :description="task.description"
          v-bind:style="{ 'background-color': color }"
        />
      </li>
    </ul>
  </div>
</template>

<script>
import Task from "../components/Task.vue";

export default {
  name: "TaskList",
  components: {
    Task,
  },
  props: ["title", "tasks", "color"],
};
</script>

<style scoped>
.task-list {
  list-style-type: none;
}

.task-list:not(:last-child) {
  border-right: thick solid;
}

li {
  display: flex;
  justify-content: center;
}
</style>