<script setup lang="ts">
import './assets/styles/styles'

import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Card from './components/Card.vue'
</script>

<template>
  <v-app>
    <Header />
    <main class="main">
      <Card />
    </main>
    <Footer />
  </v-app>
</template>

<style scoped lang="scss">
  .main {
    display: flex;
    flex-direction: column;
    gap: 32px;
    padding: 32px 24px;
  }
</style>
