<template>
  <div id="app">
    <todo-list v-bind:todos="todos"></todo-list>
  </div>
</template>

<script>
import TodoList from './components/TodoList'

export default {
  name: 'App',
  components: {
    TodoList
  },
  data() {
    return {
      todos: [
        {
          title: "Todo A",
          project: "Project A",
          completed: true
        },
        {
          title: "Todo B",
          project: "Project B",
          completed: true
        },
        {
          title: "Todo C",
          project: "Project C",
          completed: true
        },
        {
          title: "Todo D",
          project: "Project D",
          completed: false
        },
        {
          title: "Todo E",
          project: "Project E",
          completed: false
        },
        {
          title: "Todo F",
          project: "Project F",
          completed: true
        },
        {
          title: "Todo G",
          project: "Project G",
          completed: true
        },
        {
          title: "Todo H",
          project: "Project H",
          completed: false
        },
        {
          title: "Todo I",
          project: "Project I",
          completed: false
        },
        {
          title: "Todo J",
          project: "Project J",
          completed: true
        },
        {
          title: "Todo K",
          project: "Project K",
          completed: true
        },
        {
          title: "Todo L",
          project: "Project L",
          completed: false
        },
        {
          title: "Todo M",
          project: "Project M",
          completed: false
        }
      ]
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
