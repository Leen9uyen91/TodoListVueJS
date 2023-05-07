<template>
   <p class="todo-item is-completed">
       <input type="checkbox" />
       {{ todoProps.title }}
       <button class="btn-del">Delete</button>
   </p>
</template>

<script>
export default {
    name: 'TodoItem',
    props: ['todoProps']
}
</script>

<style>

</style>