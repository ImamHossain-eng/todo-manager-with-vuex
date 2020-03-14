<template>
  <div id="app">
    <div class="container">
      <div class="top">
        <AddTodo />
      <FilterTodos />
      </div>
      
      <Todos />
    </div>    
  </div>
</template>

<script>
import Todos from './components/Todos.vue'
import AddTodo from './components/AddTodos.vue'
import FilterTodos from './components/FilterTodos.vue'

export default {
  name: 'App',
  components: {
    Todos,
    AddTodo,
    FilterTodos
  }
}
</script>

<style>
body{
  background: #e8f7f0;
  line-height: 1.6;
  font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
.container{
  margin: auto;
  width: 70%;
  overflow: auto;
  padding: 0 2rem;
  text-align: center;
}
.top{
  display: grid;
  grid-template-columns: repeat(2, 1fr);
}
</style>
