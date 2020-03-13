<template>
  <div id="app">
    <div class="container">
      <Todos />
    </div>    
  </div>
</template>

<script>
import Todos from './components/Todos.vue';

export default {
  name: 'App',
  components: {
    Todos
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
</style>
