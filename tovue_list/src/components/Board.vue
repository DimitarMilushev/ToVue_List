<template>
  <div class="tasks-container">
    <div class="task-col"><TaskList title='New' :tasks="tasks.newTasks" color='#b5bab1'/></div>
    <div class="task-col"><TaskList title='In Progress' :tasks="tasks.inProgressTasks" color='#ebc334'/></div>
    <div class="task-col"><TaskList title='Done' :tasks="tasks.doneTasks" color='#80eb34'/></div>
  </div>
</template>

<script>
import TaskList from "./TaskList.vue";
export default {
  name: "Board",
  components: {
    TaskList,
  },
  data: function() {
        return {
            tasks: {
                newTasks: [
                    {
                    id: 1,
                    title: 'First Task',
                    description: 'asdasdasdasdasds'
                    },
                    {
                    id: 2,
                    title: 'Second Task',
                    description: 'asdasadasssssssssssssssssssssssssssssssssssssss'
                    },
                    {
                    id: 3,
                    title: 'Third Task',
                    description: 'asdasdasdasdasds'
                    },
                ],
                inProgressTasks: [
                    {
                    id: 1,
                    title: 'First Task',
                    description: 'asdasdasdasdasds'
                    },
                    {
                    id: 3,
                    title: 'Third Task',
                    description: 'asdasdasdasdasds'
                    },
                ],
                doneTasks: [
                    {
                    id: 1,
                    title: 'First Task',
                    description: 'asdasdasdasdasds'
                    },
                    {
                    id: 2,
                    title: 'Second Task',
                    description: 'asdasadasssssssssssssssssssssssssssssssssssssss'
                    },
                    {
                    id: 3,
                    title: 'Third Task',
                    description: 'asdasdasdasdasds'
                    },
                ]
            }
        }
    }
};
</script>

<style scoped>
.tasks-container {
    display: flex;
    justify-content: space-evenly;
}
.tasks-container .task-col {
    width: 30%;

}
</style>