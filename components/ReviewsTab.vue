<template>
  <div class="custom-scrollbar1 h-full space-y-6 overflow-y-auto pr-4">
    <h4 class="flex items-center gap-2 text-3xl font-extrabold">
      Reviews <span class="text-sm font-normal text-gray-300">( 12 )</span>
    </h4>
    <div v-for="item in 3" :key="item" class="border-b pb-4">
      <div class="flex items-center space-x-2">
        <img
          :src="`https://picsum.photos/50/50?random=${item}`"
          :alt="`Reviewer ${item}`"
          width="50"
          height="50"
          class="rounded-full"
        />
        <div>
          <h4 class="font-semibold">John Doe</h4>
          <div class="flex items-center">
            <Star
              v-for="i in 5"
              :key="i"
              :class="[
                'h-4 w-4',
                i <= 4 ? 'fill-current text-yellow-400' : 'text-gray-300',
              ]"
            />
          </div>
        </div>
      </div>
      <p class="mt-2 text-sm text-gray-600">
        Great product! The quality is excellent and it arrived earlier than
        expected. Highly recommended!
      </p>
    </div>
  </div>
</template>

<script setup>
import { Star } from "lucide-vue-next";
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
