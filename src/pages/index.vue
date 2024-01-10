<template>
    <div class="index-page">
        <h1 class="page-heading">To-Do App</h1>
        <ToDoItem/>
    </div>
</template>

<script setup>
   import ToDoItem from '../widgets/ToDo/ui/ToDoItem.vue';
</script>


<style scoped>
    .page-heading {
        color: #fff;
        text-align: left;
        display: flex;
        justify-content: center;
        width: 100dvw;
        font-size: 56px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }

    .index-page {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100dvw;
        height: 100dvh;
    }
</style>
