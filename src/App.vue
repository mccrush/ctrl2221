<template>
  <div>
    <Navbar :napravs="napravs" />

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
  },
  data() {
    return {
      razdels: ['reshens', 'napravs', 'napravs_vid', 'abouts'],
      napravs: [
        { id: '1', title: 'Видео', alias: 'video' },
        { id: '2', title: 'Интернет', alias: 'internet' },
        { id: '3', title: 'Охрана', alias: 'ohrana' }
      ]
    }
  }
}
</script>

<style>
.max-width {
  max-width: 960px;
}
</style>