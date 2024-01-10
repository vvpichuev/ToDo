<template>
    <div class="to-do-item">
       <indexCheckbox/>
       <span class="task-text"></span>
       <IndexButton><img class="close-icon" src="../../../assets/svg/close-icon.svg" alt=""></IndexButton>
    </div>
</template>

<script setup>
    import indexCheckbox from '../../../shared/TheCheckbox/ui/indexCheckbox.vue';
    import closeButton from '../../../shared/TheButton/ui/closeButton.vue';
    
</script>


<style scoped>
    .to-do-item {
        display: flex;
        align-items: center;
        gap: 10px;
        background-color: #242424;
        padding: 12px 24px;
        border-radius: 10px;
    }

    .task-text {
        width: 400px;
        border-bottom: 1px solid #fff;
    }

    .close-icon {
        width:20px;
        height: 20px;
    }
</style>
