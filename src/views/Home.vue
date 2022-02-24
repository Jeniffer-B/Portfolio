<template>
  <div class="home">
    <WelcomePage />
    <About />
  </div>
</template>

<script>
import WelcomePage from '@/components/WelcomePage.vue'
import About from '@/views/About.vue'

export default {
  name: 'Home',
  components: {
    WelcomePage,
    About
  }
}
</script>
