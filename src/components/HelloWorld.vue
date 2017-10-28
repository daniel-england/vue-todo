<template>
  <div>
    <div v-for="todo in todos">
      <p class="todo">{{ todo.text }}</p>
    </div>
    <div>{{ completedCount + '/' + todos.length }}</div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      todos: [
        {text: 'This is a task', complete: false},
        {text: 'This is a task', complete: true}
      ],
      message: 'hello'
    }
  },
  computed: {
    totalCount: function () {
      return this.todos.length;
    },
    completedCount: () => 5 // this.todos.filter(todo => todo.completed).length
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
  .todo {
    width: 300px;
    border: 1px solid blue;

  }
</style>
