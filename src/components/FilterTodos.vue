<template>
    <div class="filter">
        <p>Filter Todos:</p>
        <select @change="filterTodo($event)">
            <option value="200">200</option>
            <option value="100">100</option>
            <option value="50">50</option>
            <option value="20">20</option>
            <option value="10">10</option>
            <option value="5">5</option>
        </select>
    </div>
</template>

<script>
import { mapActions } from 'vuex'
export default {
    name: "FilterTodos",
    methods: mapActions(['filterTodo'])
}
</script>

<style scoped>
.filter{
    display:flex;
}
.filter p{
    flex: 10;
    right:0;
    padding-left:2rem;
}

select{
    border: 1px sllid #41b883;
    padding-left: 8px;
    padding-right: 5px;
    flex: 2;
}
</style>