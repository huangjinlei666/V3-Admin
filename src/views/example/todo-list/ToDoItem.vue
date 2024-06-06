<template>
  <li :class="{ completed: todo?.completed }">
    <span class="item">{{ todo?.title }}</span>
    <button @click="toggleTodo">Toggle</button>
    <button @click="deleteTodo">Delete</button>
  </li>
</template>

<script lang="ts" setup>
import { defineProps, defineEmits } from "vue"
interface Todo {
  id: number
  title: string
  completed: boolean
}
const props = defineProps({
  todo: Object as () => Todo
})
const emit = defineEmits(["toggle-todo", "delete-todo"])
const toggleTodo = () => {
  emit("toggle-todo", props.todo?.id)
}
const deleteTodo = () => {
  emit("delete-todo", props.todo?.id)
}
</script>

<style scoped>
li {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.item {
  width: 200px;
  text-overflow: ellipsis;
}
button {
  padding: 5px 10px;
  background-color: #d9534f;
  border: none;
  border-radius: 4px;
  columns: white;
  cursor: pointer;
}
button:hover {
  background-color: #c9302c;
}
.completed {
  color: #777;
  text-decoration: line-through;
}
</style>
