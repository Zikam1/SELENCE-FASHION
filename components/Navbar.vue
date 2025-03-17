<template>
  <header class="shadow-md font-serif relative">
    <div class="max-w-6xl mx-auto flex justify-between items-center py-4 px-6">
      <!-- Logo Section -->
      <div class="flex items-center">
        <img src="../assets/yu.png" alt="Selense African Fast-Fashion"
          class="h-32 w-auto object-contain md:h-20 lg:h-24 transition-transform duration-300 hover:scale-105" />
      </div>

      <!-- Navigation Links (Desktop) -->
      <nav class="hidden md:flex space-x-6">
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Shop</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Collections</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">New Arrivals</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Sale</a>
      </nav>

      <!-- Icons and Mobile Menu Button -->
      <div class="flex items-center space-x-4">
        <!-- Icons (Hidden on Mobile) -->
        <div class="hidden md:flex space-x-4">
          <button class="text-gray-700 hover:text-blue-600 text-lg transition">
            <SalesIcon />
          </button>
          <button class="text-gray-700 hover:text-blue-600 text-lg transition">
            <Search />
          </button>
          <button class="text-gray-700 hover:text-blue-600 text-lg transition">
            <Shopping />
          </button>
        </div>

      
        <button @click="isMenuOpen = !isMenuOpen" class="md:hidden text-gray-700 text-2xl focus:outline-none ml-auto">
          ☰
        </button>
      </div>
    </div>

   
    <div v-if="isMenuOpen" class="md:hidden bg-white shadow-md p-4 w-full absolute left-0 top-full transition-all duration-300">
      <nav class="flex flex-col space-y-4">
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Shop</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Collections</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">New Arrivals</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Sale</a>
      </nav>
      <div class="flex justify-end space-x-6 mt-4">
        <button class="text-gray-700 hover:text-blue-600 text-lg transition">
          <SalesIcon />
        </button>
        <button class="text-gray-700 hover:text-blue-600 text-lg transition">
          <Search />
        </button>
        <button class="text-gray-700 hover:text-blue-600 text-lg transition">
          <Shopping />
        </button>
      </div>
    </div>
  </header>
</template>

<script setup>
import SalesIcon from '@/components/icons/sales.vue';
import Search from '@/components/icons/search.vue';
import Shopping from '@/components/icons/shopping.vue';
</script>
