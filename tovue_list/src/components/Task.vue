<template>
  <div class="task">
    <h3>{{ title }}</h3>
    <hr />
    <p>{{ description }}</p>
    <hr />
  </div>
</template>

<script>
export default {
  name: "Task",
  props: ["title", "description"],
};
</script>

<style scoped>
.task {
  word-wrap: break-word;
  padding: 10px 20px;
  margin-bottom: 20px;
  cursor: pointer;
  text-align: left;
  border: 2px solid;
  border-radius: 5px;
  width: 60%;

  @media (max-width: 1200px) {
  width: 80%;
  }
  @media (max-width: 768px) {
  width: 100%;
  }
}
</style>