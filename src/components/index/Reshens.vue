<template>
  <div class="row ps-2 pe-2 pb-3">
    <h2 class="text-center mb-4">Готовые решения</h2>
    <div
      v-for="item in reshens"
      :key="item.id"
      class="
        box
        col-6 col-sm-4 col-xl-4
        d-inline-block
        shadow-sm
        rounded
        mt-2
        p-3
      "
    >
      {{ item.title }}
    </div>
  </div>
</template>

<script>
import reshens from '../../data/reshens'

export default {
  data() {
    return {
      reshens
    }
  }
}
</script>

<style scoped>
a {
  text-decoration: none;
}

.box {
  min-height: 75px;
  vertical-align: middle;
  transition: 0.3s;
}

.box:hover {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
}
</style>