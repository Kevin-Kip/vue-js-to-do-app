<template>
  <div>
    <div v-for="todo in todos">
      <div class="ui card centered">
        <div class="content" v-show="!isEditing">
          <div class="header">
            {{ todo.title }}
          </div>
          <div class="meta">
            {{ todo.project }}
          </div>
          <div class="extra-content">
          <span class="right floated edit icon" v-on:click="showForm">
            <i class="edit icon"></i>
          </span>
            <span class="right floated trash icon" v-on:click="deleteTodo(todo)">
            <i class="trash icon"></i>
          </span>
          </div>
        </div>

        <div class="content" v-show="isEditing">
          <div class="ui form">
            <div class="field">
              <label>Title</label>
              <input type="text" v-model="todo.title"/>
            </div>
            <div class='field'>
              <label>Project</label>
              <input type='text' v-model="todo.project" >
            </div>
            <div class="ui button two attached buttons">
              <button class="ui basic blue button" v-on:click="hideForm">Closse X</button>
            </div>
          </div>
        </div>
        <div class="ui button green attached bottom" v-show="!isEditing && todo.completed">
          Completed
        </div>
        <div class="ui button red attached bottom" v-show="!isEditing && !todo.completed">
          Pending
        </div>
      </div>
    </div>
  </div>
</template>

<script>
    export default {
        name: "todo",
        props: ['todos'],
        data() {
          return {
            isEditing: false
          }
        },
        methods: {
          showForm() {
            this.isEditing = true
          },
          hideForm() {
            this.isEditing = false
          },
          deleteTodo(todo) {
            this.$emit('delete-todo',todo)
          }
        }
    }
</script>

<style scoped>

</style>
