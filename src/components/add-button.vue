<template>
  <button @click="addTask">+</button>
</template>

<script>
export default {
  name: "add-button",
  methods: {
    addTask() {

      console.log('Button: I want to add a task')
    }
  }
}
</script>

<style scoped>

</style>