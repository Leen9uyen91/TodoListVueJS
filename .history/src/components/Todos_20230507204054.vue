<template>
  <AddTodo @add-todo="addTodo" />
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
import {v4 as uuidv4} from 'uuid';

export default {
   name: 'TodosBox',
   components: { TodoItem, AddTodo },
   setup() {
    const todos = ref([
        {
            id: uuidv4(),
            title: 'Việc 1',
            completed: false
        },
        {
            id: uuidv4(),
            title: 'Việc 2',
            completed: false
        },
        {
            id: uuidv4(),
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

    const addTodo = newTodo => {
        todos.value.push(newTodo)
        console.log(newTodo.id)
    }

    return {
        todos,
        markCompleted,
        addTodo
    }
   }
}
</script>

<style>

</style>