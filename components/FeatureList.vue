<template>
  <div class="max-w-7xl mx-auto px-6 py-10">
    <div class="flex flex-wrap gap-6 justify-between">
      <FeatureCard
        v-for="feature in features"
        :key="feature.id"
        :title="feature.title"
        :description="feature.description"
        :icon="feature.icon"
        class="w-full sm:w-[48%] md:w-[23%]"
      />
    </div>
  </div>
</template>

<script setup>
import FeatureCard from './FeatureCard.vue';

const features = [
  {
    id: 1,
    title:'قابل اطمینان',
    description: 'سرویس‌ها بی‌وقفه و با زمان کارکرد بیش از ۹۹٪ در کنار کسب و کار‌ها قرار دارند',
    icon: 'https://jibit.ir/wp-content/themes/jibit/images/home2/usp1.svg',
  },
  {
    id: 2,
    title: 'سریع و راحت',
    description: 'سرعت در پیاده سازی سرویس‌ها و راحتی در استفاده از آن‌ها از مزیت‌های وب‌سرویس‌هاست',
    icon: 'https://jibit.ir/wp-content/themes/jibit/images/home2/usp2.svg',
  },
  {
    id: 3,
    title: 'امنیت و حریم خصوصی',
    description: 'ارسال و پردازش درخواست‌ها با حفظ حریم خصوصی کاربران و امنیت کامل انجام می‌گیرد',
    icon: 'https://jibit.ir/wp-content/themes/jibit/images/home2/usp3.svg',
  },
  {
    id: 4,
    title: 'مقیاس پذیر',
    description: 'امکان رشد تصاعدی کسب و کار‌ها مزیتی مهم در پلتفرم ماست',
    icon: 'https://jibit.ir/wp-content/themes/jibit/images/home2/usp4.svg',
  },
];

</script>

