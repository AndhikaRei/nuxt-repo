<template>
  <div id="app">
    <Todo :todos="todos" @del-todo="deleteTodo"/>
    <AddTodo @add-todo="addTodo"/>
  </div>
</template>

<script>
import Todo from '../components/TodoComponent.vue';
import AddTodo from '../components/AddTodoComponent';
import axios from 'axios';

export default {
  name: 'Home',
  components: {
    Todo,
    AddTodo
  },
  data(){
    return {
      todos : []
    }
  },
  // methods : {
  //   deleteTodo(id){
  //     this.todos = this.todos.filter((todo) => todo.id !== id);
  //     console.log(id);
  //   },
  //   addTodo(newTodo){
  //     this.todos = [...this.todos,newTodo];
  //   }

  // }
  methods: {
    deleteTodo(id) {
      axios.delete(`https://jsonplaceholder.typicode.com/todos/${id}`)
        .then(() => this.todos = this.todos.filter(todo => todo.id !== id))
        .catch(err => console.log(err));
    },
    addTodo(newTodo) {
      const { title, completed } = newTodo;
      axios.post('https://jsonplaceholder.typicode.com/todos', {
        title,
        completed
      })
        .then(res => this.todos = [...this.todos, res.data])
        .catch(err => console.log(err));
    }
  },
  created() {
    axios.get('https://jsonplaceholder.typicode.com/todos?_limit=3')
      .then(res => this.todos = res.data)
      .catch(err => console.log(err));
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}
</style>
