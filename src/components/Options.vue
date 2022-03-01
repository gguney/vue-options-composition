
<template>
  <div class="flex--column">
    <h2>{{ title }}</h2>
    <div>{{ message }}</div>
    <div>
      <input v-model="todoInput">
      <button @click="addTodo">Add</button>
    </div>
    <ul>
      <li v-for="(todoItem, index) in todoItems" :key="index">
        {{ todoItem }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props:{
    message: {
      type: String,
      required: true
    }
  },
  data() {
    return {
      title: 'Options API',
      todoItems: [],
      todoInput: null
    }
  },
  methods:{
    addTodo(){
      this.todoItems.push(this.todoInput)
      this.todoInput = null
    }
  }
}
</script>
