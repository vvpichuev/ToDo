<template>
  <div
    :class="['checkbox', {checked: isChecked}]"
    @click="toggleCheckbox"
  >
    <img
      class="checkbox__icon"
      src="@/assets/svg/chevron.svg"
    >
  </div>
</template>

<script setup>
import {ref} from "vue";

const isChecked = ref(false)

const toggleCheckbox = () => {
  isChecked.value = !isChecked.value;
};
</script>


<style lang="scss" scoped>

  .checkbox {
    width: 16px;
    height: 16px;
    min-width: 16px;
    min-height: 16px;
    border: 2px solid $blue;
    border-radius: 15px;
    display: flex;
    align-items: center;
    justify-content: center;
    cursor: pointer;
  }

  .checked.checkbox {
    border-color: $purpledark;
    background-color: $purpledark;
  }

  .checkbox__icon {
    display: none;
  }

  .checked.checkbox .checkbox__icon  {
    display:block;
  }






</style>
