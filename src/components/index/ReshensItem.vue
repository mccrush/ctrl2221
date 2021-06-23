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
    <hr />
    <router-link
      v-for="item in napravsReshen"
      :key="item.id"
      :to="'/napravs_vid/' + item.alias"
      class="d-block"
      >{{ item.title }}</router-link
    >
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
  },
  computed: {
    napravsReshen() {
      return this.napravs_vid.filter(
        item => item.reshen.findIndex(resh => resh === this.reshen.alias) != -1
      )
    }
  }
}
</script>

<style scoped>
a {
  color: #212529;
  text-decoration: none;
}

a:hover,
a:active {
  text-decoration: underline;
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