<template>
  <footer class="bg-gray-800 text-white py-12">
    <div class="container mx-auto px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-4 gap-8">
        <!-- بخش اول: درباره ما -->
        <div>
          <h4 class="text-xl font-semibold mb-4">درباره ما</h4>
          <p class="text-gray-400">ما در xdgbit تلاش می کنیم تا بهترین خدمات پرداخت آنلاین را ارائه دهیم.</p>
        </div>
        
        <!-- بخش دوم: لینک های مفید -->
        <div>
          <h4 class="text-xl font-semibold mb-4">لینک های مفید</h4>
          <ul class="space-y-2">
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">خانه</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">خدمات</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">قیمت گذاری</a></li>
            <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">تماس با ما</a></li>
          </ul>
        </div>
        
        <!-- بخش سوم: شبکه های اجتماعی -->
        <div>
          <h4 class="text-xl font-semibold mb-4">ما را دنبال کنید</h4>
          <div class="flex space-x-4">
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path fill-rule="evenodd" d="M22 12c0-5.523-4.477-10-10-10S2 6.477 2 12c0 4.991 3.657 9.128 8.438 9.878v-6.987h-2.54V12h2.54V9.797c0-2.506 1.492-3.89 3.777-3.89 1.094 0 2.238.195 2.238.195v2.46h-1.26c-1.243 0-1.63.771-1.63 1.562V12h2.773l-.443 2.89h-2.33v6.988C18.343 21.128 22 16.991 22 12z" clip-rule="evenodd" />
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path fill-rule="evenodd" d="M12 2C6.48 2 2 6.48 2 12c0 5.52 4.48 10 10 10s10-4.48 10-10S17.52 2 12 2zm-2 8v4h2.42c.5 0 .9.37.9.86 0 .49-.4.86-.9.86H10v4h1.42c1.38 0 2.42-1.12 2.42-2.5V12h2.58c.5 0 .9-.37.9-.86 0-.49-.4-.86-.9-.86H13V8h2.42c.5 0 .9-.37.9-.86 0-.49-.4-.86-.9-.86H11.9c-.5 0-.9.37-.9.86z" clip-rule="evenodd" />
              </svg>
            </a>
            <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
              <svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
                <path fill-rule="evenodd" d="M12 2C6.48 2 2 6.48 2 12c0 5.52 4.48 10 10 10s10-4.48 10-10S17.52 2 12 2zm-2 8v4h2.42c.5 0 .9.37.9.86 0 .49-.4.86-.9.86H10v4h1.42c1.38 0 2.42-1.12 2.42-2.5V12h2.58c.5 0 .9-.37.9-.86 0-.49-.4-.86-.9-.86H13V8h2.42c.5 0 .9-.37.9-.86 0-.49-.4-.86-.9-.86H11.9c-.5 0-.9.37-.9.86z" clip-rule="evenodd" />
              </svg>
            </a>
          </div>
        </div>
        
        <!-- بخش چهارم: تماس با ما -->
        <div>
          <h4 class="text-xl font-semibold mb-4">تماس با ما</h4>
          <p class="text-gray-400">آدرس: مشهد, امام خمینی28, مجتمع مرمر</p>
          <p class="text-gray-400">تلفن: 021-12345678</p>
          <p class="text-gray-400">ایمیل: info@xdgbit.com</p>
        </div>
      </div>
      <div class="border-t border-gray-700 mt-8 pt-8 text-center text-gray-500">
        &copy; 1404 xdgbit. تمامی حقوق محفوظ است.
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
/* استایل های کامپوننت */
</style>
