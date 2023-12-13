<template>
  <div>
    <input type="checkbox" v-mode="taskData.done"> <span :class="{done: taskData.done }">{{ taskData.taskName }}</span>
  </div>
</template>

<script>
export default {
  name: 'TodoList',
  props: [
    'taskData'
  ]
}
</script>

<style>
.done{
  text-decoration: line-through;
}
</style>
