<template>
  <div class="flex--column">
    <h2>{{ title }}</h2>
    <div>{{ message }}</div>
    <div>
      <input v-model="todo.todoInput">
      <button @click="addTodo">Add</button>
    </div>
    <ul>
      <li v-for="(todoItem, index) in todo.todoItems" :key="index">
        {{ todoItem }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { reactive } from 'vue'

const todo = reactive({ todoInput: null, todoItems: [] })
const title = 'Composition API'

defineProps({
  message: String
})

function addTodo() {
  todo.todoItems.push(todo.todoInput)
  todo.todoInput = null
}
</script>

