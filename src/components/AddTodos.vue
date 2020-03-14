<template>
    <div>
        <div id="form">
            <form @submit="onSubmit">
                <input type="text" v-model="title" placeholder="Add Todo.....">
                <input type="submit" value="Submit">
            </form>

        </div>
    </div>
</template>
<script>
import { mapActions } from 'vuex'
export default {
    Name: "AddTodo",
    data() {
        return {
            title: ''
        }
    },
    methods: {
        ...mapActions(['addTodo']),
        onSubmit(e){
            e.preventDefault();
            this.addTodo(this.title);
            this.title ='';
        }
    }
}
</script>
<style scoped>
#form{
    display: flex;
    width: 100%;
}
input[type="text"]{
    flex: 10;
    border: 1px solid #262626;
    padding: .7rem;
    outline: 0;
}
input[type="submit"]{
    flex:2;
    color: #efefef;
    background: #262626;
    padding: .7rem;
    cursor: pointer;
}
input[type="submit"]:hover{
    color:#262626;
    background:#fff
}


</style>