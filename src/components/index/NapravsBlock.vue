<template>
  <div class="row ps-2 pe-2 pb-3">
    <h2 class="text-center mb-4">Направления работы</h2>

    <router-link
      v-for="item in napravs"
      :key="item.id"
      class="
        box
        col-6 col-sm-4 col-xl-4
        d-inline-block
        text-center
        shadow-sm
        rounded
        mt-2
        p-3
      "
      :to="'/napravs/' + item.alias"
    >
      <img
        :src="'/img/index/' + item.alias + '.svg'"
        class="img-napr"
        width="75"
        :alt="item.title"
      />
      <br />
      {{ item.title }}
    </router-link>
  </div>
</template>

<script>
import napravs from '@/data/napravs'

export default {
  data() {
    return {
      napravs
    }
  }
}
</script>

<style scoped>
a {
  color: #024c89;
  text-decoration: none;
}

.box {
  min-height: 150px;
  vertical-align: middle;
  transition: 0.3s;
}

.box:hover {
  box-shadow: 0 0.5rem 1rem rgba(0, 0, 0, 0.15) !important;
}

.img-napr {
  margin: 10px 0 20px 0;
}
</style>