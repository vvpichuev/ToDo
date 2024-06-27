<template>
  <input
    v-model="description"
    type="text"
    @keyup="addTodo"
  >
</template>

<script setup>
import {computed} from "vue";

const props = defineProps({
  modelValue: {
    type: String,
    required: true
  }
})

const emit = defineEmits('update:modelValue');

const description = computed({
  get() {
    return props.modelValue;
  },
  set(value) {

    emit('update:modelValue', value)
  }
})



</script>
<style scoped>

</style>
