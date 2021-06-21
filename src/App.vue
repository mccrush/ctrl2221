<template>
  <div>
    <Navbar />

    <div class="container pt-4">
      <router-view v-slot="{ Component }">
        <component :is="Component" />
      </router-view>

      <!-- <transition name="fade" mode="out-in">
        <Footer />
      </transition> -->
    </div>
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.min.css'
import Navbar from '@/components/Navbar'

export default {
  components: {
    Navbar
  }
}
</script>

<style>
.max-width {
  max-width: 960px;
}
</style>