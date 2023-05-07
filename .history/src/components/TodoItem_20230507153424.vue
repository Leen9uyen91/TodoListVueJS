<template>
   <p class="todo-item is-completed" :id="my-id">
       <input type="checkbox" />
       {{ todoProps.title }}
       <button class="btn-del">Delete</button>
   </p>
</template>

<script>
import { ref } from 'vue';
export default {

    name: 'TodoItem',
    props: ['todoProps'],
    setup() {
        const new_id = ref('my-new-id')
        return {
            new_id
        }
    }
}
</script>

<style>
   .btn-del {
        background: red;
        color: #fff;
        border: none;
        cursor: pointer;
        float: right;
   }
   .todo-item {
        background: #f4f4f4;
        padding: 10px;
        margin: 0;
        border-bottom: 1px #ccc dotted;
   }

   .is-completed {
       text-decoration: line-through;
   }

</style>