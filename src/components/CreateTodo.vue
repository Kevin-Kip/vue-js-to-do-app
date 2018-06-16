<template>
  <form>
    <input type="text" v-bind="titleToSave"/><br>
    <input type="text" v-bind="projectToSave"/><br>
    <input type="text" v-bind="completedToSave"/><br>
    <button class="ui button" v-on:click="saveTodo">Save</button>
  </form>
</template>

<script>
    export default {
        name: "create-todo",
        props: ['todos'],
        data() {
          return {
            titleToSave: null,
            projectToSave: null,
            completedToSave: null
          }
        },
      methods: {
          saveTodo() {
              todos.push({
                title: titleToSave,
                project:  projectToSave,
                completed: completedToSave
              })
          }
      }
    }
</script>

<style scoped>

</style>
