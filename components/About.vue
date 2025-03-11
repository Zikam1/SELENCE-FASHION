<template>
    <div class="mt-8 md:pb-24">
      <h3 class="text-xl md:text-3xl font-bold text-gray-900 mb-8 text-center">
        Who Can Join?
      </h3>
      <div class="grid grid-cols-1 md:grid-cols-3 gap-6 max-w-4xl mx-auto"> <!-- Added max-w-4xl and mx-auto -->
        <!-- Designer Card -->
        <div class="group relative overflow-hidden bg-white rounded-xl shadow-md hover:shadow-lg transition-shadow duration-300 animate-fade-in">
          <div class="p-8">
            <div class="flex items-center justify-center w-12 h-12 bg-indigo-50 rounded-full mb-4">
              <svg class="w-6 h-6 text-indigo-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
              </svg>
            </div>
            <h4 class="text-xl font-semibold text-gray-900 mb-2">Designers</h4>
            <p class="text-gray-600">Collaborate and showcase your talent.</p>
          </div>
          <div class="absolute inset-0 bg-indigo-600 opacity-0 group-hover:opacity-10 transition-opacity duration-300"></div>
        </div>
  
        <!-- Shopper Card -->
        <div class="group relative overflow-hidden bg-white rounded-xl shadow-md hover:shadow-lg transition-shadow duration-300 animate-fade-in">
          <div class="p-8">
            <div class="flex items-center justify-center w-12 h-12 bg-indigo-50 rounded-full mb-4">
              <svg class="w-6 h-6 text-indigo-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z"></path>
              </svg>
            </div>
            <h4 class="text-xl font-semibold text-gray-900 mb-2">Shoppers</h4>
            <p class="text-gray-600">Discover affordable, high-quality fashion.</p>
          </div>
          <div class="absolute inset-0 bg-indigo-600 opacity-0 group-hover:opacity-10 transition-opacity duration-300"></div>
        </div>
  
        <!-- Investor Card -->
        <div class="group relative overflow-hidden bg-white rounded-xl shadow-md hover:shadow-lg transition-shadow duration-300 animate-fade-in">
          <div class="p-8">
            <div class="flex items-center justify-center w-12 h-12 bg-indigo-50 rounded-full mb-4">
              <svg class="w-6 h-6 text-indigo-600" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8c-1.657 0-3 .895-3 2s1.343 2 3 2 3 .895 3 2-1.343 2-3 2m0-8c1.11 0 2.08.402 2.599 1M12 8V7m0 1v8m0 0v1m0-1c-1.11 0-2.08-.402-2.599-1M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
              </svg>
            </div>
            <h4 class="text-xl font-semibold text-gray-900 mb-2">Investors</h4>
            <p class="text-gray-600">Support the future of African fashion.</p>
          </div>
          <div class="absolute inset-0 bg-indigo-600 opacity-0 group-hover:opacity-10 transition-opacity duration-300"></div>
        </div>
      </div>
    </div>
  </template>
  
  <style>
  .animate-fade-in {
    animation: fadeIn 0.5s ease-in-out;
  }
  
  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }
  </style>