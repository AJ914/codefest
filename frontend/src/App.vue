<template>
  <div class="min-h-screen bg-gray-100">
    <Navbar />
    <Home />
  </div>
</template>

<script>
import Home from './pages/Home.vue';
import Navbar from './components/Navbar.vue';

export default {
  components: {
    Home,
    Navbar
  }
};
</script>
