<template>
  <header class="w-full bg-white shadow-md">
    <div class="container mx-auto flex items-center justify-between py-4 px-6">
      <!-- Logo -->
      <nuxt-link to="/" class="text-2xl font-bold text-gray-900">
        FashionX
      </nuxt-link>

      <!-- Navigation Links -->
      <nav class="hidden md:flex space-x-6">
        <nuxt-link to="/" class="nav-link">Home</nuxt-link>
        <nuxt-link to="/shop" class="nav-link">Shop</nuxt-link>
        <nuxt-link to="/collections" class="nav-link">Collections</nuxt-link>
        <nuxt-link to="/about" class="nav-link">About</nuxt-link>
        <nuxt-link to="/contact" class="nav-link">Contact</nuxt-link>
      </nav>

      <!-- Search, Cart & Profile -->
      <div class="flex items-center space-x-4">
        <input
          type="text"
          placeholder="Search..."
          class="hidden md:block px-3 py-2 border rounded-md focus:outline-none"
        />

        <nuxt-link to="/cart" class="relative">
          <i class="ri-shopping-bag-line text-2xl"></i>
          <span class="absolute -top-1 -right-2 bg-red-500 text-white text-xs px-1.5 py-0.5 rounded-full">2</span>
        </nuxt-link>

        <nuxt-link to="/profile">
          <i class="ri-user-line text-2xl"></i>
        </nuxt-link>

        <!-- Mobile Menu Button -->
        <button @click="toggleMenu" class="md:hidden">
          <i class="ri-menu-line text-2xl"></i>
        </button>
      </div>
    </div>

    <!-- Mobile Menu -->
    <div v-if="menuOpen" class="md:hidden bg-white shadow-md">
      <nav class="flex flex-col p-4 space-y-3">
        <nuxt-link to="/" class="nav-link">Home</nuxt-link>
        <nuxt-link to="/shop" class="nav-link">Shop</nuxt-link>
        <nuxt-link to="/collections" class="nav-link">Collections</nuxt-link>
        <nuxt-link to="/about" class="nav-link">About</nuxt-link>
        <nuxt-link to="/contact" class="nav-link">Contact</nuxt-link>
      </nav>
    </div>
  </header>
</template>

<script setup>
import { ref } from "vue";

const menuOpen = ref(false);

const toggleMenu = () => {
  menuOpen.value = !menuOpen.value;
};
</script>

<style scoped>
.nav-link {
  @apply text-gray-700 hover:text-black transition;
}
</style>
