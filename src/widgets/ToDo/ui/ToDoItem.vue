<template>
    <div class="to-do-item">

      <div class="checkbox">
        <input type="checkbox" id="custom-checkbox">
        <label for="custom-checkbox"></label>
      </div>

      <input class="task-text-field" type="text">
      <button><img src="@/assets/svg/delete_icon.svg" alt=""></button>
    </div>
</template>

<script setup>
    import indexCheckbox from '../../../shared/TheCheckbox/ui/index.vue';
    import indexInput from '../../../shared/TheInput/ui/index.vue';
    import IndexButton from '../../../shared/TheButton/ui/index.vue';
    
</script>


<style lang="scss" scoped>
    .to-do-item {
      width: 740px;
      padding: 16px;
      border-radius: 8px;
      background-color: #333333;
      display: flex;
      justify-content: space-between;
      border: 1px solid #5E60CE;

      input[type="checkbox"] {
        display: none;
      }

      label {
        display: block;
        position: relative;
        width: 16px;
        height: 16px;
        border: 2px solid #4EA8DE;
        border-radius: 50%;
        cursor: pointer;
      }

      input[type="checkbox"]:checked + label::after {
        content: url('@/assets/svg/cheked.svg');
        display: block;
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        border-radius: 50%;
        width: 16px;
        height: 16px;
        background-color: #5E60CE;
      }

      .task-text-field {
        max-width: 630px;
        width: 100%;
        outline: none;
        background-color: transparent;
        border: none;
        color: white;
      }
    }
</style>
