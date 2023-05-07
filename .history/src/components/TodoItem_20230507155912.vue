<template>
   <p :class="['todo-item', todoProps.completed ? 'is-completed' : '']">
       <input type="checkbox" :checked="todoProps.completed" v-on:change="markItemCompleted"/>
       {{ todoProps.title }}
       <button class="btn-del">Delete</button>
   </p>
</template>

<script>

export default {

    name: 'TodoItem',
    props: ['todoProps'],
    setup() {
        const markItemCompleted = () => {
            console.log('mark')
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