<!-- <template>
  <div class="py-10 bg-gray-50">
    <div class="max-w-7xl mx-auto px-6 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-center text-gray-900 mb-6">
        xdgbitسرویس های 
      </h2>

      <div v-if="isClient">
        <Swiper
          :modules="[Autoplay, Pagination]"
          :slides-per-view="1"
          :loop="true"
          :autoplay="{ delay: 2000, disableOnInteraction: false }"
          pagination
          class="rounded-lg shadow-md"
          style="height: 200px;"
        >
          <SwiperSlide
            v-for="(slide, index) in slides"
            :key="index"
            class="p-6 bg-white flex flex-col justify-center items-center text-center"
          >
            <h3 class="text-xl font-semibold text-gray-800 mb-3">{{ slide.title }}</h3>
            <p class="text-gray-600">{{ slide.description }}</p>
          </SwiperSlide>
        </Swiper>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';
const isClient = ref(false);

onMounted(() => {
  isClient.value = true;
});

import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';

const slides = [
  { title: "سرویس 1", description: "توضیحات مختصر درباره سرویس 1." },
  { title: "سرویس 2", description: "توضیحات مختصر درباره سرویس 2." },
  { title: "سرویس 3", description: "توضیحات مختصر درباره سرویس 3." },
  { title: "سرویس 4", description: "توضیحات مختصر درباره سرویس 4." },
  { title: "سرویس 5", description: "توضیحات مختصر درباره سرویس 5." }
];
</script> -->

<template>
  <div class="py-10 bg-gray-50">
    <div class="max-w-7xl mx-auto px-6 sm:px-6 lg:px-8">
      <h2 class="text-3xl font-bold text-center text-gray-900 mb-6">
        xdgbitسرویس های
      </h2>

      <div class="flex justify-center gap-4 mb-6">
        <button
          v-for="(slide, index) in slides.slice(0,4)"
          :key="index"
          @click="goToSlide(index)"
          :class="[
            'px-4 py-2 rounded-md cursor-pointer',
            activeIndex === index ? 'bg-blue-600 text-white' : 'bg-gray-200 text-gray-700',
          ]"
        >
          {{ slide.title }}
        </button>
      </div>

      <div v-if="isClient">
        <Swiper
          @swiper="onSwiper"
          @slideChange="onSlideChange"
          :modules="[Autoplay, Pagination]"
          :slides-per-view="1"
          :loop="true"
          :autoplay="{ delay: 2000, disableOnInteraction: false }"
          pagination
          class="rounded-lg shadow-md"
          style="height: 200px;"
        >
          <SwiperSlide
            v-for="(slide, index) in slides"
            :key="index"
            class="p-6 bg-white flex flex-col justify-center items-center text-center"
          >
            <h3 class="text-xl font-semibold text-gray-800 mb-3">{{ slide.title }}</h3>
            <p class="text-gray-600">{{ slide.description }}</p>
          </SwiperSlide>
        </Swiper>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue';

import { Swiper, SwiperSlide } from 'swiper/vue';
import { Autoplay, Pagination } from 'swiper/modules';
import 'swiper/css';
import 'swiper/css/pagination';

const isClient = ref(false);
const swiper = ref(null);
const activeIndex = ref(0);

onMounted(() => {
  isClient.value = true;
});

const slides = [
  { title: "سرویس 1", description: "توضیحات مختصر درباره سرویس 1." },
  { title: "سرویس 2", description: "توضیحات مختصر درباره سرویس 2." },
  { title: "سرویس 3", description: "توضیحات مختصر درباره سرویس 3." },
  { title: "سرویس 4", description: "توضیحات مختصر درباره سرویس 4." },
  { title: "سرویس 5", description: "توضیحات مختصر درباره سرویس 5." }
];

function onSwiper(swiperInstance) {
  swiper.value = swiperInstance;
}

function onSlideChange() {
  if (swiper.value) {
    activeIndex.value = swiper.value.realIndex;
  }
}

function goToSlide(index) {
  if (swiper.value) {
    swiper.value.slideToLoop(index);
  }
}
</script>

