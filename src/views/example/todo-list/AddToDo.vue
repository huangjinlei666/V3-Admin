<template>
  <div>
    <input v-model.trim="todoElement" @keyup.enter="submitTodo" />
    <button @click="submitTodo">Add</button>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue"
const todoElement = ref("")
const emit = defineEmits(["add-todo"])
const submitTodo = () => {
  if (todoElement.value) {
    emit("add-todo", todoElement.value)
    todoElement.value = ""
  }
}
</script>

<style scoped>
div {
  margin-bottom: 20px;
  text-align: center;
}
input {
  padding: 10px;
  border: 1px solid #ddd;
  border-radius: 4px;
  width: 70%;
  margin-right: 10px;
}
button {
  padding: 10px 15px;
  background-color: #5cb85c;
  border: none;
  border-radius: 4px;
  color: white;
  cursor: pointer;
}

button:hover {
  background-color: #4cae4c;
}
</style>
