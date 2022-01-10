<template>
    <b-list-group-item>
        <span v-if="todo.done" class="done">{{ todo.text}}</span>
        <span v-else>{{todo.text}}</span>
         <b-button class="float-right ml-3" pill variant="outline-danger" @click="completeDelete">Delete</b-button> 
        <span v-if="todo.done" class="float-right">&#128077;</span>       
         <b-button v-else class="float-right" pill variant="outline-success" @click="completeTodo">&#10003;</b-button> 
    </b-list-group-item>
    
</template>
<script>


export default {
    name: "TodoItem",
    props: {
        todo: {
        type: Object,
        required: true
        }
    },
    methods: {
        completeTodo() {
            this.$emit("todo-completed", this.todo);
        },
          completeDelete() {
                this.$emit("todo-deleted", this.todo);
            }
     
    }
}
</script>
<style>
.done{
    text-decoration: line-through;
}

</style>
