<template>
  <div class="add-task">
    <input type="text" placeholder="Название задачи">
    <add-button></add-button>
  </div>
</template>

<script>
import addButton from './add-button.vue'

export default {
  name: "new-task",
  components: {
    addButton
  },
}
</script>

<style scoped>

</style>