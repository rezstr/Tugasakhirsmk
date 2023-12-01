<script lang="ts" setup>
import type { Products } from '~/types/products';
const products = ref<Products[]>([]);
const totalPrice = computed(() => {
return products.value.filter((product) => product.price !==
undefined).reduce((accumulator, currentValue) => accumulator +
currentValue.price!, 0);
})
onMounted(() => {
let localStorageData = localStorage.getItem("products");
if (localStorageData) {
products.value = JSON.parse(localStorageData);
}
})
</script>

<template>
  <section>
    <div class="container">
      <div class="py-10 flex gap-6">
        <div class="w-[70%]">
          <div
            class="flex justify-between items-center pb-7 border-b border- gray-300 mb-6"
          >
            <h1 class="text-3xl font-medium">Shopping Cart</h1>
            <p class="text-3xl font-medium">0 Items</p>
          </div>
          <div class="flex flex-col gap-6">
            <CardsCardCart />
          </div>
        </div>
        <div class="w-[30%] bg-white shadow-xl h-max p-6">
          <h3 class="text-xl font-medium mb-6">Order Summary</h3>
          <div class="flex flex-col gap-3 border-b border-gray-300 pb-4">
            <div>
              <div class="flex gap-4 items-center">
                <span class="text-limit limit-1 text-sm"
                  >Men's Streetwear Fashion</span
                >
                <span class="text-sm font-semibold">$30</span>
              </div>
            </div>
          </div>
          <div class="pt-4 flex items-center justify-between mb-6">
            <span class="text-base">Total</span>
            <span class="text-base font-bold">$30</span>
          </div>

          <button
            class="bg-blue-600 text-white text-base font-bold w-full py- 2 rounded-lg"
          >
            Checkout
          </button>
        </div>
      </div>
    </div>
  </section>
</template>
