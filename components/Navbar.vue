<template>
  <header class="bg-white shadow-lg border-b border-gray-100 sticky top-0 z-50">
    <nav class="container mx-auto flex justify-between items-center py-4 px-6 lg:px-8">
      <!-- لوگو -->
      <div class="flex items-center">
        <div class="text-3xl font-black text-blue-600 tracking-tight">xdgbit</div>
      </div>
      
      <!-- منوی اصلی -->
      <ul class="hidden lg:flex gap-8 text-gray-700 font-medium">
        <li><a href="#" class="hover:text-blue-600 transition-colors duration-200 py-2">سرویس ها</a></li>
        <li><NuxtLink to="/contact" class="hover:text-blue-600 transition-colors duration-200 py-2">ارتباط با ما</NuxtLink></li>
        <li><a href="#" class="hover:text-blue-600 transition-colors duration-200 py-2">بلاگ</a></li>
        <li><NuxtLink to="/" class="hover:text-blue-600 transition-colors duration-200 py-2">خانه</NuxtLink></li>
      </ul>

      <!-- دکمه‌های عمل -->
      <div class="flex items-center gap-4">
        <button class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-200">
          ورود
        </button>
        <button class="bg-blue-600 text-white px-6 py-2 rounded-lg hover:bg-blue-700 transition-colors duration-200 font-medium">
          ثبت‌نام
        </button>
        
        <!-- منوی موبایل -->
        <button class="lg:hidden text-gray-700">
          <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"></path>
          </svg>
        </button>
      </div>
    </nav>
  </header>
</template>
