<template>
    <div>
        <h1 class="header">Todos List</h1>
        <div class="todos">
            <div v-for="todo in allTodos" :key="todo.id" class="todo">
                <h4>{{todo.title}}
                    <i @click="deleteTodo(todo.id)" class="fa fa-trash"></i>
                </h4>
            </div>
        </div>
    </div>
</template>
<script>
import { mapGetters, mapActions } from 'vuex';

export default {
    name: "Todos",
    methods: {
        ...mapActions(['fetchTodos', 'deleteTodo'])
    },
    computed: mapGetters(['allTodos']),
    created() {
        this.fetchTodos();
    }
}
</script>
<style scoped>
.header{
    background: #262626;
    color: #efefef;
}
.todos{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 1rem;
}
.todo{
    border: 1px solid #ccc;
    background: #41b883;
    padding: 1rem;
    text-align: center;
    position: relative;
}
i{
    position: absolute;
    bottom: 10px;
    right: 10px;
    color: #fff;
    cursor: pointer;
}

</style>