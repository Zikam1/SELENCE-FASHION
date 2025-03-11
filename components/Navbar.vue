<template>
  <header class="bg-white shadow-md font-serif">
    <div class="max-w-6xl mx-auto flex justify-between items-center py-4 px-6">
      <!-- Logo Section -->
      <div class="flex items-center">
        <img src="../assets/yu.png" alt="Selense African Fast-Fashion"
          class="h-64 w-auto object-contain md:h-20 lg:h-24 transition-transform duration-300 hover:scale-105" />
      </div>

      <!-- Navigation Links -->
      <nav class="hidden md:flex space-x-6">
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Shop</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Collections</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">New Arrivals</a>
        <a href="#" class="text-gray-700 hover:text-blue-600 text-base font-medium transition">Sale</a>
      </nav>

      <!-- Icons (Search, Cart, User) -->
      <div class="flex items-center space-x-4">
        <button class="text-gray-700 hover:text-blue-600 text-lg transition"><span>🔍</span></button>
        <button class="text-gray-700 hover:text-blue-600 text-lg transition"><span>🛒</span></button>
        <button class="text-gray-700 hover:text-blue-600 text-lg transition"><span>👤</span></button>
      </div>
    </div>
  </header>
</template>
