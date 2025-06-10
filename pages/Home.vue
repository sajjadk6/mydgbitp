<template>
  <div>
    <Navbar />
    <HeroSection />
    <FeatureList />
    <ServiceSlider />
    <Footer />
  </div>
</template>

<script>
import Navbar from '~/components/Navbar.vue'
import HeroSection from '~/components/HeroSection.vue'
import FeatureList from '~/components/FeatureList.vue'
import ServiceSlider from '~/components/ServiceSlider.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Navbar,
    HeroSection,
    FeatureList,
    ServiceSlider,
    Footer
  }
}
</script>
