<template>
  <form @submit="addItem">
     <input type="text" placeholder="Việc mới..." 
       v-model="title"
     />
     <input type="submit" value="Thêm" class="add-btn">
  </form>
</template>

<script>
import { ref } from 'vue';

export default {
   name: 'AddTodo',
   setup() {
    const title = ref('')
    
    const addItem = event =>{
        event.preventDefault();

        const newItem = {
            id: 4,
            title: title.value,
            complated: false
        }

        context.emit('add-todo', newItem)
    }
    return {
        title,
        addItem
    }
   }
}
</script>

<style scoped>
   form {
    display: flex;
   }
   input[type='text'] {
    flex: 10;
    padding: 5px;
   }
   input[type='submit'] {
    flex: 2;
   }
</style>