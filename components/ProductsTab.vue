<template>
  <div
    class="custom-scrollbar1 h-full space-y-3 overflow-y-auto pr-2 lg:space-y-6 lg:pr-4"
  >
    <h4
      class="flex items-center gap-1 text-lg font-bold lg:gap-2 lg:text-3xl lg:font-extrabold"
    >
      Products
      <span class="text-xs font-normal text-gray-300 lg:text-sm">( 12 )</span>
    </h4>
    <div
      v-for="item in 5"
      :key="item"
      class="flex items-start space-x-2 border-b pb-3 lg:space-x-4 lg:pb-4"
    >
      <div class="relative">
        <img
          :src="`https://picsum.photos/80/80?random=${item}`"
          :alt="`Product ${item}`"
          width="80"
          height="80"
          class="rounded-md lg:h-[127px] lg:w-[145px] lg:rounded-3xl"
        />
        <div
          class="absolute bottom-0 right-0 rounded-br-[2000px] rounded-tl-md bg-pink-500 px-1.5 py-0.5 text-[8px] leading-tight text-white lg:rounded-br-[6000px] lg:rounded-tl-full lg:px-7 lg:py-3 lg:text-xs"
        >
          Live Auction
        </div>
      </div>
      <div class="flex-1 min-w-0">
        <div class="flex items-start justify-between">
          <h3
            class="text-xs font-medium truncate pr-1 lg:text-lg lg:font-normal"
          >
            Six-Piece Clothing Set (Blouse - Pants - Hat And ...)
          </h3>
          <button
            class="flex-shrink-0 text-gray-400 hover:text-pink-500 focus:outline-none"
            aria-label="Add to favorites"
          >
            <Heart class="h-4 w-4 lg:h-6 lg:w-6" />
          </button>
        </div>
        <p class="mt-0.5 text-xs text-gray-500 lg:mt-1 lg:text-lg">
          Starting Price
          <span class="text-sm font-bold text-black lg:text-2xl">1000 EGP</span>
        </p>
        <div class="mt-1 lg:mt-2">
          <span class="text-[10px] text-gray-500 lg:text-lg lg:mr-2"
            >Lot Starts In
          </span>
          <div
            class="flex lg:inline-flex mt-0.5 items-center space-x-1 lg:mt-2 lg:space-x-2"
          >
            <span
              class="rounded-full bg-orange-100 px-2 py-0.5 text-[10px] font-medium text-orange-500 lg:px-5 lg:pb-2 lg:pt-1 lg:text-sm"
            >
              <span class="font-bold lg:text-xl">2</span> Days
            </span>
            <span
              class="rounded-full bg-orange-100 px-2 py-0.5 text-[10px] font-medium text-orange-500 lg:px-5 lg:pb-2 lg:pt-1 lg:text-sm"
            >
              <span class="font-bold lg:text-xl">10</span> Hours
            </span>
            <span
              class="rounded-full bg-orange-100 px-2 py-0.5 text-[10px] font-medium text-orange-500 lg:px-5 lg:pb-2 lg:pt-1 lg:text-sm"
            >
              <span class="font-bold lg:text-xl">50</span> Minutes
            </span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { Heart } from "lucide-vue-next";
</script>

<style scoped>
.custom-scrollbar1 {
  scrollbar-width: thin;
  scrollbar-color: #d1d5db #f3f4f6;
}

.custom-scrollbar1::-webkit-scrollbar {
  width: 4px;
}

.custom-scrollbar1::-webkit-scrollbar-track {
  background: #f3f4f6;
}

.custom-scrollbar1::-webkit-scrollbar-thumb {
  background-color: #d1d5db;
  border-radius: 20px;
  border: 1px solid #f3f4f6;
}

@media (min-width: 1024px) {
  .custom-scrollbar1::-webkit-scrollbar {
    width: 8px;
  }

  .custom-scrollbar1::-webkit-scrollbar-thumb {
    border: 3px solid #f3f4f6;
  }
}
</style>
