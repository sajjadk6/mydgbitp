<template>
  <div class="min-h-screen flex flex-col">
    <!-- استفاده از Navbar کامپوننت -->
    <Navbar />

    <main class="flex-grow container mx-auto px-4 py-10">
      <h1 class="text-3xl font-bold mb-8 text-right">ارتباط با ما</h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
        <!-- فرم تماس -->
        <form @submit.prevent="submitForm" class="space-y-6 bg-white p-8 rounded shadow-md text-right">
          <div>
            <label for="name" class="block mb-2 font-semibold">نام و نام خانوادگی</label>
            <input
              v-model="form.name"
              type="text"
              id="name"
              class="w-full border border-gray-300 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="نام و نام خانوادگی خود را وارد کنید"
              required
            />
          </div>

          <div>
            <label for="email" class="block mb-2 font-semibold">ایمیل</label>
            <input
              v-model="form.email"
              type="email"
              id="email"
              class="w-full border border-gray-300 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="example@email.com"
              required
            />
          </div>

          <div>
            <label for="subject" class="block mb-2 font-semibold">موضوع</label>
            <input
              v-model="form.subject"
              type="text"
              id="subject"
              class="w-full border border-gray-300 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="موضوع پیام خود را وارد کنید"
              required
            />
          </div>

          <div>
            <label for="message" class="block mb-2 font-semibold">پیام</label>
            <textarea
              v-model="form.message"
              id="message"
              rows="5"
              class="w-full border border-gray-300 rounded px-3 py-2 focus:outline-none focus:ring-2 focus:ring-blue-500"
              placeholder="پیام خود را بنویسید"
              required
            ></textarea>
          </div>

          <button
            type="submit"
            class="bg-blue-600 text-white font-bold py-2 px-6 rounded hover:bg-blue-700 transition"
          >
            ارسال
          </button>
        </form>

        <!-- اطلاعات تماس -->
        <div class="space-y-6 bg-white p-8 rounded shadow-md text-right">
          <h2 class="text-2xl font-semibold mb-4">اطلاعات تماس</h2>

          <p><strong>آدرس:</strong> تهران، خیابان مثال، پلاک ۱۲۳</p>
          <p><strong>تلفن:</strong> ۰۲۱-۱۲۳۴۵۶۷۸</p>
          <p><strong>ایمیل:</strong> info@jibit.ir</p>
          <p><strong>ساعات کاری:</strong> شنبه تا چهارشنبه، ۹ صبح تا ۵ عصر</p>
        </div>
      </div>
    </main>

    <!-- استفاده از Footer کامپوننت -->
    <Footer />
  </div>
</template>

<script setup>
import Navbar from '~/components/Navbar.vue'
import Footer from '~/components/Footer.vue'

import { reactive } from 'vue'

const form = reactive({
  name: '',
  email: '',
  subject: '',
  message: ''
})

const submitForm = () => {
  // اینجا میتونی ارسال فرم به API یا هر منطق دیگه رو اضافه کنی
  alert(`پیام شما ارسال شد!\nنام: ${form.name}\nایمیل: ${form.email}\nموضوع: ${form.subject}\nپیام: ${form.message}`)
  // پاک کردن فرم بعد از ارسال
  form.name = ''
  form.email = ''
  form.subject = ''
  form.message = ''
}
</script>

<style scoped>
/* اگر لازم بود اینجا استایل های اختصاصی اضافه کن */
</style>
