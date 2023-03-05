

<template>
  <div class="container">
    <h4>Today's tasks</h4>
    <ul class="tasks">
      <to-do-item
          v-for="text in texts"
          :todo="text"
          :key="text.id"
      ></to-do-item>
      <new-task></new-task>


    </ul>
  </div>

</template>


<script>
import toDoItem from './components/to-do-item.vue'
import newTask from './components/new-task.vue'

export default {
  name: 'App',
  data() {
    return {
      todos: [
        { id: 0, text: 'Create To-Do-App in Vue.js' },
        { id: 1, text: 'Send it to Vladik'}
      ],
    }
  },
  methods: {
    addNewTodo() {
      this.todos.push({
        id: this.nextTodoId++,
        title: this.newTodoText
      })
      this.newTodoText = ''
    }
  }
  components: {
    toDoItem,
    newTask
  }
}
</script>


