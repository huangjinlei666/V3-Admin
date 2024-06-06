<template>
  <div>
    <h1>Todo List</h1>
    <AddToDo @add-todo="addNewTodo" />
    <ToDoList :todos="todos" @toggle-todo="toggleTodo" @delete-todo="deleteTodo" />
  </div>
</template>
<script lang="ts" setup>
import { reactive } from "vue"
import AddToDo from "./AddToDo.vue"
import ToDoList from "./ToDoList.vue"
interface Todo {
  id: number
  title: string
  completed: boolean
}

const todos = reactive<Todo[]>([])
const addNewTodo = (newTodo: string) => {
  const isRepeat = todos.find((item) => item.title === newTodo)
  if (isRepeat) {
    alert("已添加")
  } else {
    todos.push({ id: todos.length + 1, title: newTodo, completed: false })
  }
}

const toggleTodo = (todoId: number) => {
  const todo = todos.find((item) => item.id === todoId)
  if (todo) {
    todo.completed = !todo.completed
  }
}

const deleteTodo = (todoId: number) => {
  const index = todos.findIndex((item) => item.id === todoId)
  if (index !== -1) {
    todos.splice(index, 1)
  }
}
</script>
<style scoped>
body {
  font-family: "Arial", sans-serif;
  background-color: #f4f4f4;
  margin: 0;
  padding: 0;
  display: flex;
  justify-content: center;
  height: 100vh;
  align-items: center;
}

#app {
  background: white;
  padding: 20px;
  border-radius: 8px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  width: 400px;
}

h1 {
  text-align: center;
  color: #333;
}
</style>
