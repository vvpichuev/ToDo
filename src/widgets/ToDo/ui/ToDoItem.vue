<template>
    <div class="to-do-item">

      <div class="checkbox">
        <input type="checkbox" id="custom-checkbox">

        <label for="custom-checkbox"></label>
      </div>
      <TheInput class="task-text-field" v-model="task.text" />
      <button class="delete_button"><img class="delete_icon" src="@/assets/svg/delete.svg" alt=""></button>
    </div>
</template>

<script setup>
import TheInput from '@/shared/TheInput/ui/index.vue';

const props = defineProps({
  task: {
    type: Object,
    required: true
  }
})


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

      .delete_button {
        background-color: transparent;
        outline: none;
        border: none;

        .delete_icon {
          width: 18px;
          height: 18px;
        }

      }
    }
</style>
