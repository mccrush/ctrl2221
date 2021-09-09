<template>
  <div class="box dropdown d-inline-block ps-0 pe-0">
    <h4
      class="resh-head h-100 pt-4 ps-3 pe-3"
      :id="reshen.id"
      data-bs-toggle="dropdown"
    >
      {{ reshen.title }}
    </h4>
    <div
      class="
        dropdown-menu
        position-absolute
        bg-white
        rounded
        shadow-sm
        border-0
        p-3
      "
      :class="{ 'to-right': reshen.pos === 'right' }"
      :aria-labelledby="reshen.id"
    >
      <router-link
        v-for="item in napravsReshen"
        :key="item.id"
        :to="'/napravs_vid/' + item.alias"
        class="d-block"
        >{{ item.title }}</router-link
      >
    </div>
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

.to-right {
  right: 0;
  text-align: right;
}

.dropdown-menu {
  margin-top: -42px;
}

.dropdown:hover div.dropdown-menu {
  display: block;
}
</style>