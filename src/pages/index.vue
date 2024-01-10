<template>
    <div class="index-page">
        <h1 class="page-heading">To-Do App</h1>
        <div class="add-new-task">
            <indexInput/>
            <Button>Add task </Button>
        </div>
        <ToDoItem/>
    </div>
</template>

<script setup>
   import ToDoItem from '../widgets/ToDo/ui/ToDoItem.vue';
   import indexInput from '../shared/TheInput/ui/indexInput.vue';
   import Button from '../shared/TheButton/ui/Button.vue';
</script>


<style scoped>

.index-page {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        width: 100dvw;
        height: 100dvh;
        gap: 20px;
    }
    .page-heading {
        color: #fff;
        text-align: left;
        display: flex;
        justify-content: center;
        width: 100dvw;
        font-size: 56px;
        font-family: Verdana, Geneva, Tahoma, sans-serif;
    }

    .add-new-task {
        display: flex;
        gap: 10px;
        width: 500px;
    }
</style>
