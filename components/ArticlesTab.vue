<template>
  <div class="custom-scrollbar1 h-full space-y-6 overflow-y-auto pr-4">
    <h4 class="flex items-center gap-2 text-3xl font-extrabold">
      Articles <span class="text-sm font-normal text-gray-300">( 12 )</span>
    </h4>
    <div v-for="item in 3" :key="item" class="border-b pb-4">
      <h3 class="text-lg font-semibold">How to Choose the Perfect Outfit</h3>
      <p class="mt-2 text-sm text-gray-500">
        Discover the secrets to selecting the ideal ensemble for any occasion.
        This comprehensive guide will help you navigate...
      </p>
      <a href="#" class="mt-2 inline-block text-sm text-pink-500">Read more</a>
    </div>
  </div>
</template>

<script setup>
// No additional imports needed for this component
</script>

<style scoped>
.custom-scrollbar1 {
  scrollbar-width: thin;
  scrollbar-color: #d1d5db #f3f4f6;
}

.custom-scrollbar1::-webkit-scrollbar {
  width: 8px;
}

.custom-scrollbar1::-webkit-scrollbar-track {
  background: #f3f4f6;
}

.custom-scrollbar1::-webkit-scrollbar-thumb {
  background-color: #d1d5db;
  border-radius: 20px;
  border: 3px solid #f3f4f6;
}
</style>
