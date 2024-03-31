<script setup lang="ts">
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Breadcrumbs from './components/Breadcrumbs.vue'
import Card from './components/Card.vue'
//
</script>

<template>
  <v-app>
    <Header />
    <main class="main">
      <Breadcrumbs />
      <Card />
    </main>
    <Footer />
  </v-app>
</template>

<style scoped lang="scss">
  .main {
    margin-top: 32px;
    padding: 0 24px;
  }
</style>
