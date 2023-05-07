<template>
  <TodoItem />
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
        }
    ])

    return {
        todos
    }
   }
}
</script>

<style>

</style>