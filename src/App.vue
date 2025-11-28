<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import { ref, nextTick, onMounted, defineComponent } from 'vue';
import Navbar from './components/Navbar.vue';
import Hero from './components/Hero.vue';
import Services from './components/Services.vue';
import About from './components/About.vue';
import ExperienceSkills from './components/ExperienceSkills.vue';
import Projects from './components/Projects.vue';
import Contact from './components/Contact.vue';
import Footer from './components/Footer.vue';
import BackToTop from './components/BackToTop.vue';
import LoadingSpinner from './components/LoadingSpinner.vue';

export default defineComponent ({
  name: 'App',
  components: {
    Navbar,
    Hero,
    Services,
    About,
    ExperienceSkills,
    Projects,
    Contact,
    Footer,
    BackToTop,
    LoadingSpinner
  },

  setup() {
    const loading = ref(true);

    onMounted(async () => {
      await nextTick();

      AOS.init({
        duration: 800,
        once: false,
        offset: 100,
        easing: 'ease-in-out',
      });

      setTimeout(() => {
        loading.value = false;
      }, 800);

    });

    return { loading };
  }
})

</script>

<template>
  <div v-if="loading">
    <LoadingSpinner />
  </div>

  <div v-else class="min-h-screen bg-linear-to-br from-gray-900 via-blue-900 to-gray-900">
    <Navbar />
    <Hero />
    <Services />
    <About />
    <ExperienceSkills />
    <Projects />
    <Contact />
    <Footer />
    <BackToTop />
  </div>
</template>

<style scoped>
</style>
