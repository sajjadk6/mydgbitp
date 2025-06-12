<!-- <template>
  <div class="min-h-screen flex flex-col">
    <Navbar />

    <main class="flex-grow container mx-auto px-4 py-10">
      <h1 class="text-3xl font-bold mb-8 text-right">ارتباط با ما</h1>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-10">
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

        <div class="space-y-6 bg-white p-8 rounded shadow-md text-right">
          <h2 class="text-2xl font-semibold mb-4">اطلاعات تماس</h2>

          <p><strong>آدرس:</strong> تهران، خیابان مثال، پلاک ۱۲۳</p>
          <p><strong>تلفن:</strong> ۰۲۱-۱۲۳۴۵۶۷۸</p>
          <p><strong>ایمیل:</strong> info@jibit.ir</p>
          <p><strong>ساعات کاری:</strong> شنبه تا چهارشنبه، ۹ صبح تا ۵ عصر</p>
        </div>
      </div>
    </main>

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
  alert(`پیام شما ارسال شد!\nنام: ${form.name}\nایمیل: ${form.email}\nموضوع: ${form.subject}\nپیام: ${form.message}`)
  form.name = ''
  form.email = ''
  form.subject = ''
  form.message = ''
}
</script>

<style scoped>
</style> -->


<template>
  <div>
    <Navbar />

    <section class="py-16 bg-gray-50 min-h-screen">
      <div class="container mx-auto px-6 md:px-12">
        <h2 class="text-3xl font-semibold text-gray-800 mb-12 text-center md:text-right">ارتباط با ما</h2>

        <div class="flex flex-col md:flex-row gap-12 max-w-6xl mx-auto">
          <!-- نقشه سمت چپ -->
          <div class="md:flex-1 rounded-lg overflow-hidden shadow-lg h-[400px] md:h-auto">
            <iframe
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3240.1987345143496!2d51.41592781525821!3d35.735556780190335!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3f8df94e4a25a529%3A0x5c44c7c7ec84b62a!2z2KfZhNin2YrYqti22YbYsdio2KfYsSDYp9mE2YLYsdi12KfYqtmK2YXYqtiq2LHYp9mE2KfYqiDZhtmF2KfYqg!5e0!3m2!1sfa!2s!4v1687923502399!5m2!1sfa!2s"
              width="100%"
              height="100%"
              style="border:0;"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            ></iframe>
          </div>

          <!-- بخش اطلاعات تماس سمت راست -->
          <div class="md:flex-[0.6] bg-white rounded-lg shadow-lg p-8 text-gray-700 flex flex-col justify-center">
            <ul class="space-y-8">
              <li class="flex items-start gap-4">
                <span class="material-icons text-blue-600 text-4xl mt-1">location_on</span>
                <div>
                  <h4 class="font-semibold text-lg mb-1">آدرس دفتر مرکزی</h4>
                  <p>تهران، تیموری، خیابان شهید احمد قاسمی، خیابان آزاده، پلاک ۰، برج فناوری طرشت، طبقه ۱۰، واحد ۱۰۰۴</p>
                  <p class="mt-1 text-sm text-gray-500">کد پستی: ۱۴۵۹۹۶۵۲۲۳</p>
                </div>
              </li>

              <li class="flex items-start gap-4">
                <span class="material-icons text-blue-600 text-4xl mt-1">phone</span>
                <div>
                  <h4 class="font-semibold text-lg mb-1">تلفن پشتیبانی</h4>
                  <p>۰۲۱-۴۲۲۹۶</p>
                  <p class="mt-1 text-sm text-gray-500">شنبه تا چهارشنبه: ۸:۰۰ تا ۱۸:۰۰</p>
                </div>
              </li>

              <li class="flex items-start gap-4">
                <span class="material-icons text-blue-600 text-4xl mt-1">email</span>
                <div>
                  <h4 class="font-semibold text-lg mb-1">ایمیل پشتیبانی</h4>
                  <p>support@jibit.ir</p>
                </div>
              </li>

              <li class="flex items-start gap-4">
                <span class="material-icons text-blue-600 text-4xl mt-1">chat</span>
                <div>
                  <h4 class="font-semibold text-lg mb-1">تلگرام پشتیبانی</h4>
                  <p>@Jibit_Support</p>
                  <p class="mt-1 text-sm text-gray-500">شنبه تا چهارشنبه: ۸:۰۰ تا ۲۴:۰۰<br>پنج‌شنبه و جمعه: ۹:۰۰ تا ۲۰:۰۰</p>
                </div>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <Footer />
  </div>
</template>

<script setup>
import Navbar from '@/components/Navbar.vue';
import Footer from '@/components/Footer.vue';
</script>

<style scoped>
.material-icons {
  font-family: 'Material Icons';
}
</style>
