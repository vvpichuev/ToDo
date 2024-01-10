<template>
   <button class="button"><slot/></button>
</template>

<script setup>

</script>


<style scoped>
   .button {
      display: flex;
      justify-content: center;
      align-items: center;
      background-color: transparent;
      outline: none;
      border: none;
      width: 24px;
      height: 24px;
   }
</style>
