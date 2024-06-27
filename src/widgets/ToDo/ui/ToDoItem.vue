<template>
  <div class="to-do-item">
    <TheCheckbox />
    <TheInput
      v-model="task.text"
      class="task-text-field"
    />
    <button class="delete_button">
      <img
        class="delete_icon"
        src="@/assets/svg/delete.svg"
        alt=""
      >
    </button>
  </div>
</template>

<script setup>
import TheCheckbox from "@/shared/TheCheckbox/ui/index.vue";
import TheInput from "@/shared/TheInput/ui/index.vue";

const props = defineProps({
  task: {
    type: Object,
    required: true,
  },
});
</script>

<style lang="scss" scoped>
.to-do-item {
  width: 740px;
  padding: 16px;
  border-radius: 8px;
  background-color: #333333;
  display: flex;
  justify-content: space-between;
  border: 1px solid #5e60ce;

  //@include media($xs){
  //  max-width: 240px;
  //}
  //
  //@include media($s){
  //  min-width: 310px;
  //  max-width: 400px;
  //}

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
