<script setup lang="ts">
import Navbar from '../components/NavBar.vue'
import Hero from '../components/Hero.vue'
import Menu from '@/components/Menu.vue';
import Footer from '@/components/Footer.vue';
</script>

<template>
  <main>
    <header>
      <Navbar />
    </header>

    <body>
      <div class="container">
        <!-- Hero -->
        <Hero />
        <div class="row">
          <div class="col">
            <div class="new-catalogs-title">
              <p>Explore Our Catalogs</p>
              <Menu />
            </div>
          </div>
        </div>
        <br>  
      </div>
    </body>
    <footer>
        <Footer />
    </footer>
  </main>
</template>
