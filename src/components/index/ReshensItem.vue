<template>
  <div class="box d-inline-block rounded ps-0 pe-0">
    <h4 class="h-100 pt-4 ps-3 pe-3">{{ reshen.title }}</h4>
    <!-- <hr />
    <router-link
      v-for="item in napravsReshen"
      :key="item.id"
      :to="'/napravs_vid/' + item.alias"
      class="d-block"
      >{{ item.title }}</router-link
    > -->
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
  min-height: 90px;
  vertical-align: middle;
  cursor: pointer;
  transition: 0.3s;
}

.box:hover {
  /* box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important; */
}
</style>