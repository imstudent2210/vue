<template>
  <div>
    <img alt="Vue logo" src="./assets/logo.png">
    <div>
      <p>Two way binding in Vue</p>
    <div v-show="isShow">
      <p>Two way binding in Vue</p>
    </div>
    <button @click="isShow = !isShow">Hidden</button>
    <button @click="count++">Count</button>
    {{ count }}
    </div>

    <h2 :class="{redText: isTrue}">fesfesfetre</h2>
    <button @click="isTrue = !isTrue">Add Class Binding</button>
    <input type="text" v-model="arr[0]">

    {{ object.id }}

    <div>
      <ul>
        <li v-for="(item, index) in arr" :key="index">{{ item }}</li>
      </ul>
    </div>
    <div>
      <input type="text" v-model="newTask">
      <button @click="listObject.push({ taskName: newTask, done: false })">Add task</button>
      <div v-for="(object, index) in listObject" :key="index">
        <input type="checkbox" v-model="object.done"> <span :class="{done: object.done }">{{ object.taskName }}</span>
      </div>
  </div>
  <!-- <TodoList v-for="(object, index) in listObject" :key="index" :taskData="object"/> -->
  </div>
</template>

<script>
// import TodoList from './components/Vue1312.vue'
export default {
  name: 'App',
  components: {
    // TodoList
  },
  data () {
    return {
      isShow: true,
      count: 0,
      isTrue: false,
      arr: [
        'item 1',
        'item 2',
        'item 3',
        'item 4'
      ],
      object: {
        id: '001'
      },
      newTask: '',
      listObject: [
        { taskName: 'task1', done: false },
        { taskName: 'task2', done: false },
        { taskName: 'task3', done: true },
        { taskName: 'task4', done: false }]
    }
  },
  updated () {
    return {
      count: 2
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
.redText{
  color: red;
}
.done{
  text-decoration: line-through;
}
</style>
