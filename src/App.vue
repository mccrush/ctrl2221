<template>
  <div>
    <Navbar :napravs="napravs" />

    <div
      class="
        max-width-780
        container
        bg-white
        rounded-bottom
        pt-3
        ps-4
        pe-4
        pb-1
      "
    >
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
      razdels: ['reshens', 'napravs', 'napravs_vid', 'abouts']
    }
  }
}
</script>

<style>
body {
  background: #f8f9fa;
}

.max-width-960 {
  max-width: 960px;
}

.max-width-780 {
  max-width: 780px;
}

.btn:focus,
.btn-check:focus + .btn-outline-dark,
.form-control:focus,
.form-select:focus,
.accordion-button:focus,
.navbar-toggler:focus {
  outline: 0 !important;
  box-shadow: none !important;
}
</style>