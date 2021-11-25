<template>
    <div class="borderBold">
    <ul>
        <TodoListItem v-for="todo in todos" :key="todo.id"
        :item="todo"
        @toggle="toggleListItem"/>
    </ul> 
    </div>
</template>

<script>
import TodoListItem from "./TodoListItem";
export default { 
    data: () => ({
        todos:[
            {id: 1, finished: false, name: "Vue Js lernen"},
            {id: 1, finished: true, name: "Code Beispiele üben"},
            {id: 1, finished: false, name: "Git commit"},
            {id: 1, finished: true, name: "Ein weiteres Todo"}]
    }),
    name: "TodoList",
    components: {
        TodoListItem,
    },
    methods:{
        toggleListItem(el){
            el.finished = !el.finished;
        }
    }
}
</script>

<style>

.finishedTask{
  text-decoration: line-through;
}

button{
    color: blue;
}
</style>