<template>
  <div id="app">
     <Header/>
     <AddTodo/>
   <Todos v-bind:todos="todos" v-on:del-todo="deleteTodo"/>
  
  </div>
</template>

<script>
import Todos from './components/Todos'
import Header from './components/layout/Header'
import AddTodo from './components/AddTodo'

export default {
  name: 'App',
  components: {
  Todos,
  Header,
  AddTodo
  },
  methods:{
    deleteTodo(id){
this.todos= this.todos.filter(todo=>todo.id !==id)
    }
  },
  data(){
    return{
      todos:[
        {
          id:1,
          title:"To do 1",
          completed: false
        },
        {
          id:2,
          title:"To do two",
          completed: true
        },
        {
          id:3,
          title:"To do three",
          completed: false
        }
      ]
    }
  }
}
</script>

<style>
*{
  box-sizing:border-box;
  margin:0;
  padding:0;
}
body{
  font-family: Arial, Helvetica, sans-serif;
  line-height:1.4;
}
.btn{
  display: inline-block;
  border: none;
  background: #555;
  color: #fff;
  padding: 7px 20px;
  cursor: pointer;
}
.btn:hover{
  background: #666;
}
</style>
