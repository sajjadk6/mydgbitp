<template>
  <div>
    <Navbar />
    <router-view></router-view>
  </div>
</template>

<script setup>

import Home from './pages/Home.vue'
import { Navbar } from './components/Navbar.vue'
</script>
