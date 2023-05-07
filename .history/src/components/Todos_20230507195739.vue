<template>
  <AddTodo />
  <TodoItem 
    v-for="todo in todos" 
    :key="todo.id" 
    :todoProps="todo" 
    @item-completed="markCompleted"
  />
</template>

<script>
import { ref } from 'vue';
import TodoItem from './TodoItem.vue';
import AddTodo from './AddTodo.vue';

export default {
   name: 'TodosBox',
   components: { TodoItem, AddTodo },
   setup() {
    const todos = ref([
        {
            id: 1,
            title: 'Việc 1',
            completed: false
        },
        {
            id: 2,
            title: 'Việc 2',
            completed: false
        },
        {
            id: 3,
            title: 'Việc 3',
            completed: false
        }
    ])

    const markCompleted = id => {
        todos.value = todos.value.map(todo => {
             if(todo.id === id) todo.completed = !todo.completed;
             return todo
        })
    }

    return {
        todos,
        markCompleted
    }
   }
}
</script>

<style>

</style>