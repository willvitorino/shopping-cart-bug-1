<script setup>
import ShoppingCart from './components/ShoppingCart.vue';
</script>
<template>
  <div
    class="flex flex-col items-center justify-center dark:text-white h-screen w-screen"
  >
    <ShoppingCart />

    <span class="text-sm mt-8">
      by <a href="https://github.com/willvitorino" target="_blank" class="text-blue-500 hover:underline">William Vitorino</a>
    </span>
  </div>
</template>
