<script setup>
defineProps({
  product: {
    type: Object,
    required: true
  }
})

defineEmits(['increase-quantity', 'decrease-quantity'])
</script>

<template>
  <li class="flex flex-col my-2 w-full odd:bg-gray-100 odd:dark:bg-gray-700 p-4">
    <span class="flex items-center justify-between w-full space-x-3">
      <span class="w-1/3 truncate">{{ product.name }}</span>
      <span>
        {{ Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format((product.price) / 100) }}
      </span>
      <span class="inline-flex items-center justify-between space-x-3">
        <button
          class="bg-blue-400 py-1 px-2 rounded-md cursor-pointer hover:bg-blue-600"
          :class="{
            '!opacity-50 !cursor-not-allowed': product.quantity === 0,
            'hover:bg-blue-600': product.quantity > 0,
          }"
          :disabled="product.quantity === 0"
          @click="$emit('decrease-quantity', product)"
        >
          -
        </button>
        <span class="w-12 text-center">{{ product.quantity }}</span>
        <button
          class="bg-blue-400 hover:bg-blue-600 py-1 px-2 rounded-md"
          @click="$emit('increase-quantity', product)"
        >
          +
        </button>
      </span>
      <span class="w-16 text-right">
        {{ Intl.NumberFormat('pt-BR', { style: 'currency', currency: 'BRL' }).format((product.price * product.quantity) / 100) }}
      </span>
    </span>
  </li>
</template>
