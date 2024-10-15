<template>
  <div>
    <section class="bg-dark d-flex align-items-center justify-content-center text-light">
      <h3>section 1</h3>
    </section>
    <section class="bg-danger d-flex align-items-center justify-content-center text-light">
      <h3>section 2</h3>
    </section>
    <section class="bg-primary d-flex align-items-center justify-content-center text-light">
      <h3>section 3</h3>
    </section>
    <section class="bg-warning d-flex align-items-center justify-content-center text-light">
      <h3>section 4</h3>
    </section>
    <section class="bg-success d-flex align-items-center justify-content-center text-light">
      <h3>section 5</h3>
    </section>
  </div>
  <transition name="slide-fade">
    <GoToUp v-if="scroll > 400"/>
  </transition>
</template>

<script setup>
import { ref } from 'vue';
import GoToUp from './components/GoToUp.vue';

const scroll = ref(null)
document.addEventListener('scroll',()=>{
  scroll.value = document.documentElement.scrollTop
  
})
</script>

<style>
section {
  height: 100vh;
}

.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.8s cubic-bezier(1, 0.5, 0.8, 1);
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateY(20px);
  opacity: 0;
}
</style>
