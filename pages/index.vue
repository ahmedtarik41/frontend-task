<template>
  <div class="min-h-screen bg-gray-100" style="direction: ltr">
    <!-- Header -->
    <header class="bg-white shadow">
      <div
        class="container mx-auto flex items-center justify-between px-4 py-4"
      >
        <div class="flex items-center space-x-4">
          <button @click="isMenuOpen = !isMenuOpen" class="lg:hidden">
            <Menu class="text-gray-600" />
          </button>
          <img
            src="https://picsum.photos/120/40"
            alt="Mazaady Logo"
            width="120"
            height="40"
          />
          <nav class="hidden space-x-4 lg:flex">
            <a
              href="#"
              class="border-b-2 border-pink-500 pb-2 font-semibold text-pink-500"
              >Home</a
            >
            <a href="#" class="text-gray-600 hover:text-pink-500">Blog</a>
            <a href="#" class="text-gray-600 hover:text-pink-500">Gifts</a>
          </nav>
        </div>
        <div class="flex items-center space-x-4">
          <button class="rounded-full p-2 hover:bg-gray-100">
            <Search class="h-5 w-5 text-gray-400" />
          </button>
          <div class="hidden h-6 w-px bg-[#FFEAD2] lg:block"></div>
          <button class="rounded-full p-2 hover:bg-gray-100">
            <Bell class="h-5 w-5 text-gray-400" />
          </button>
          <div class="hidden h-6 w-px bg-[#FFEAD2] lg:block"></div>
          <img
            src="https://picsum.photos/40/40"
            alt="User Avatar"
            width="40"
            height="40"
            class="rounded-full"
          />
          <button
            class="hidden items-center space-x-1 rounded-xl bg-gradient-to-r from-[#d20653] to-[#ff951d] px-4 py-2 text-sm font-bold text-white lg:flex"
          >
            <span class="rounded-full border border-white">
              <Plus class="h-3 w-3" />
            </span>
            <span>Add New Product</span>
          </button>
          <button class="hidden items-center space-x-1 text-gray-600 lg:flex">
            <Globe class="mr-1 h-5 w-5" />
            <div class="hidden h-6 w-px bg-[#FFEAD2] lg:block"></div>
            <span>EN</span>
          </button>
        </div>
      </div>
    </header>

    <!-- Mobile Menu -->
    <nav v-if="isMenuOpen" class="bg-white shadow-lg md:hidden">
      <div class="container mx-auto px-4 py-4">
        <ul class="space-y-2">
          <li>
            <a href="#" class="block font-semibold text-pink-500">Home</a>
          </li>
          <li><a href="#" class="block text-gray-600">Blog</a></li>
          <li><a href="#" class="block text-gray-600">Gifts</a></li>
          <li>
            <button class="flex items-center space-x-1 text-gray-600">
              <Globe class="mr-1 h-5 w-5" />
              <div class="h-6 w-px bg-[#FFEAD2]"></div>
              <span>EN</span>
            </button>
          </li>
        </ul>
      </div>
    </nav>

    <!-- Main Content -->
    <main class="container mx-auto px-4 py-8 lg:flex lg:space-x-8">
      <div class="lg:w-1/3">
        <!-- User Profile -->
        <div class="mb-6 rounded-lg bg-white p-6 shadow">
          <div class="flex flex-col items-start">
            <img
              src="https://picsum.photos/200/200"
              alt="Hala Ahmed"
              width="100"
              height="100"
              class="mb-4 rounded-3xl object-cover"
            />
            <h2 class="mb-3 text-2xl font-bold">Hala Ahmed</h2>
            <p class="mb-6 text-sm">
              I am Hala Ahmed, I am the owner of the local brand called Beauty
              which is for Makeup and Skin Care.
            </p>
          </div>

          <div class="mb-6 flex gap-x-4">
            <div
              class="flex w-full items-center space-x-2 rounded-2xl bg-orange-50 px-3 py-2"
            >
              <UserPlus class="h-5 w-5 text-orange-500" />
              <div>
                <span class="block text-sm font-bold text-black">5</span>
                <span class="text-xs text-orange-500">Following</span>
              </div>
            </div>
            <div
              class="flex w-full items-center space-x-2 rounded-2xl bg-orange-50 px-3 py-2"
            >
              <Users class="h-5 w-5 text-orange-500" />
              <div>
                <span class="block text-sm font-bold text-black">20</span>
                <span class="text-xs text-orange-500">Followers</span>
              </div>
            </div>
            <div
              class="flex w-full items-center space-x-2 rounded-2xl bg-orange-50 px-3 py-2"
            >
              <Star class="h-5 w-5 text-orange-500" />
              <div>
                <div class="block text-sm font-bold text-black">
                  4.2
                  <span
                    class="hidden sm:inline text-xs font-normal text-[#828282]"
                    >( 15 )</span
                  >
                </div>
                <span class="text-xs text-orange-500">Rate</span>
              </div>
            </div>
          </div>

          <button
            class="w-full rounded-xl bg-gradient-to-r from-[#d20653] to-[#ff951d] py-2 text-white"
          >
            Follow
          </button>
        </div>

        <!-- QR Code -->
        <div class="mb-6 rounded-lg bg-white p-6 shadow lg:mb-0">
          <div class="mb-4 flex items-center justify-between">
            <h3 class="text-2xl font-bold">QR Code</h3>
            <div class="flex items-center space-x-6">
              <button class="text-black" aria-label="View QR Code">
                <Eye class="h-6 w-6" />
              </button>
              <button class="text-black" aria-label="Share QR Code">
                <Share2 class="h-6 w-6" />
              </button>
              <button class="text-black" aria-label="Download QR Code">
                <Download class="h-6 w-6" />
              </button>
              <button
                class="block lg:!hidden"
                @click="isQRCodeExpanded = !isQRCodeExpanded"
                :aria-expanded="isQRCodeExpanded"
                aria-controls="qr-code-content"
              >
                <ChevronUp v-if="isQRCodeExpanded" class="text-gray-600" />
                <ChevronDown v-else class="text-gray-600" />
              </button>
            </div>
          </div>

          <div
            id="qr-code-content"
            :class="{
              'block lg:hidden': isQRCodeExpanded,
              'hidden lg:block': !isQRCodeExpanded,
            }"
          >
            <div
              class="mb-4 flex items-center gap-2 bg-orange-50 px-4 py-[18px]"
            >
              <Download class="h-6 w-6 text-orange-500" />
              <div class="text-normal text-xs">
                Download the QR code or share it with your friends.
              </div>
            </div>
            <div
              class="rounded-3xl bg-gradient-to-r from-[#d20653] to-[#ff951d] p-6"
            >
              <div class="flex flex-col items-center rounded-2xl bg-white p-4">
                <img
                  src="https://picsum.photos/120/40"
                  alt="Mazaady Logo"
                  width="120"
                  height="40"
                />
                <p class="my-2 text-center text-2xl font-bold">Hala Ahmed</p>
                <img
                  src="https://picsum.photos/135/135"
                  alt="QR Code"
                  width="135"
                  height="135"
                  class="mx-auto"
                />
                <p class="mt-2 text-center text-sm text-black">
                  Follow Us On Mazaady
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- Right Column -->
      <div class="overflow-y-hidden rounded-lg bg-white p-6 shadow lg:w-2/3">
        <!-- Tabs -->
        <div class="mb-6 flex items-center justify-between">
          <div class="flex space-x-4">
            <button
              v-for="tab in ['products', 'articles', 'reviews']"
              :key="tab"
              @click="activeTab = tab"
              :class="[
                'rounded-2xl px-4 py-2',
                activeTab === tab
                  ? 'border border-orange-500 bg-orange-50 font-bold text-orange-400'
                  : 'border border-gray-300 text-sm font-normal text-gray-500',
              ]"
            >
              {{ tab.charAt(0).toUpperCase() + tab.slice(1) }}
            </button>
          </div>
          <button
            class="hidden items-center space-x-1 rounded-xl bg-gradient-to-r from-[#d20653] to-[#ff951d] px-4 py-2 text-sm font-bold text-white lg:flex"
          >
            <span class="rounded-full border border-white">
              <Plus class="h-3 w-3" />
            </span>
            <span>Add Review</span>
          </button>
        </div>

        <!-- Tab Content -->
        <div class="h-full pb-6">
          <component :is="activeTabComponent" />
        </div>
      </div>
    </main>
  </div>
</template>

<script setup>
import { ref, computed } from "vue";
import {
  Menu,
  Bell,
  Search,
  ChevronUp,
  ChevronDown,
  Eye,
  Share2,
  Download,
  Heart,
  Star,
  Plus,
  Globe,
  Users,
  UserPlus,
} from "lucide-vue-next";
import ProductsTab from "./components/ProductsTab.vue";
import ArticlesTab from "./components/ArticlesTab.vue";
import ReviewsTab from "./components/ReviewsTab.vue";

const isMenuOpen = ref(false);
const isQRCodeExpanded = ref(false);
const activeTab = ref("products");

const activeTabComponent = computed(() => {
  switch (activeTab.value) {
    case "products":
      return ProductsTab;
    case "articles":
      return ArticlesTab;
    case "reviews":
      return ReviewsTab;
    default:
      return null;
  }
});
</script>

<style scoped>
/* Add any component-specific styles here */
</style>
