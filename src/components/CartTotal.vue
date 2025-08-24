<script setup>
defineProps({
  total: {
    type: Number,
    required: true
  }
})
</script>

<template>
  <p class="flex items-center justify-between text-3xl mt-4 p-8">
    <span>Total:</span>
    <span class="font-bold">{{ Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format(total/100) }}</span>
  </p>
</template>
