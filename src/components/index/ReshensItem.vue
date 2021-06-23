<template>
  <div
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
    {{ reshen.title }}
  </div>
</template>

<script>
import napravs_vid from '@/data/napravs_vid'

export default {
  props: {
    reshen: Object
  },
  data() {
    return {
      napravs_vid
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