<template>
  <TodoItem 
    v-for="todo in todos" 
    v-bind:key="todo.id" 
    v-bind:todoProps="todo" 
    v-on:item-completed="markCompleted"
  />
</template>

<script>
import { ref } from 'vue';
import TodoItem from './TodoItem.vue';

export default {
   name: 'TodosBox',
   components: { TodoItem },
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
        console.log(id)
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