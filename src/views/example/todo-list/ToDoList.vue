<template>
  <ul>
    <ToDoItem v-for="todo in todos" :key="todo.id" :todo="todo" @toggle-todo="toggleTodo" @delete-todo="deleteTodo" />
  </ul>
</template>

<script lang="ts" setup>
import { defineProps, defineEmits } from "vue"
import ToDoItem from "./ToDoItem.vue"
interface Todo {
  id: number
  title: string
  completed: boolean
}
const props = defineProps({
  todos: Array as () => Todo[]
})
const emit = defineEmits(["toggle-todo", "delete-todo"])
const toggleTodo = (id: number) => {
  emit("toggle-todo", id)
}
const deleteTodo = (id: number) => {
  emit("delete-todo", id)
}
</script>

<style scoped>
ul {
  list-style-type: none;
  padding: 0;
}
li {
  padding: 10px;
  border-bottom: 1px solid #ddd;
}

li:last-child {
  border-bottom: none;
}
</style>
