<template>
  <div id="app">
    <TodoList :todos="todos" @delete-item='deleteItem'/>
  </div>
</template>

<script>
  import TodoList from '@/components/TodoList'

  export default{
    name: 'App',
    data() {
      return {
          todos: ['TV', 'Playstation', 'VR 360'] 
        }
    },
    components: {
      TodoList
    },
    methods: {
      deleteItem(index) {
        this.todos.splice(index, 1);
      }
    }
  }
</script>

<style>

</style>
