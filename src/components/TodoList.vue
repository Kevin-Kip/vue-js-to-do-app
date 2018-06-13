<template>
  <div>
    <p align="center">Completed tasks: {{ todos.filter(todo => {return todo.completed === true}).length }} </p>
    <p align="center"> Pending tasks: {{ todos.filter(todo => {return todo.completed === false}).length }}</p>
    <todo v-for="todoItem in todos" v-bind="todoItem" v-bind:key="todoItem.title"></todo>
  </div>
</template>

<script>

  import Todo from './Todo'

    export default {
        props: ['todos'],
        components: {
          Todo
        },
        methods: {
          deleteTodo(todo) {
            const todoIndex = this.todos.indexOf(todo);
            this.todos.splice(todoIndex, 1)
          }
        }
    }
</script>

<style scoped>

</style>
