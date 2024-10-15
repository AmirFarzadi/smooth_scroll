<template>
  <button id="jsHandle" class="bg-light border-0 rounded-circle" @click="GoToUpHandler">
    <i class="bi bi-arrow-up-circle fs-3"></i>
  </button>
</template>

<script setup>
// import { ref } from 'vue';

function GoToUpHandler(){
    document.documentElement.scrollTop = 0
}
</script>

<style scoped>
#jsHandle{
    position: fixed;
    bottom: 30px;
    right: 50px;
    width: 50px;
    height: 50px;
}
</style>