<script setup>
import { computed, ref } from "vue";
import ProductItem from './ProductItem.vue';
import CartTotal from './CartTotal.vue';

const products = ref([
  { id: 1, name: "Mouse - Logitech MX Master 3S", price: 9220, quantity: 1 },
  { id: 2, name: "Keyboard - Logitech MX Keys", price: 7990, quantity: 1 },
  {
    id: 3,
    name: "WebCam - Logitech HD Pro Webcam C920",
    price: 6890,
    quantity: 1,
  },
]);

const total = computed(() => {
  return products.value.reduce((acc, product) => acc + product.price * product.quantity, 0,);
});

function increaseQuantity(product) {
  product.quantity += 1;
}

function decreaseQuantity(product) {
  if (product.quantity === 0) {
    return;
  }

  product.quantity -= 1;
}
</script>

<template>
  <div class="max-w-3xl w-full border border-gray-50 dark:border-gray-600 shadow-2xl rounded-md">
    <h2 class="text-4xl bg-gray-600 p-8 text-gray-200">Shopping Cart</h2>
    <ul class="dark:text-white p-8">
      <ProductItem
        v-for="product in products"
        :key="product.id"
        :product="product"
        @increase-quantity="increaseQuantity"
        @decrease-quantity="decreaseQuantity"
      />
    </ul>
    <CartTotal :total="total" />
  </div>
</template>
