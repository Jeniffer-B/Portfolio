<template>
  <div class="home">
    <WelcomePage />
    <About />
    <Projects />
    <Contact />
  </div>
</template>

<script>
import WelcomePage from '@/components/WelcomePage.vue'
import About from '@/views/About.vue'
import Projects from '@/views/Projects.vue'
import Contact from '@/views/Contact.vue'

export default {
  name: 'Home',
  components: {
    WelcomePage,
    About,
    Projects,
    Contact
  }
}
</script>

