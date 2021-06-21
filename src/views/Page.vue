<template>
  <h1>{{ naprav.title }}</h1>
  <p>
    Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet itaque eaque
    eos cumque libero excepturi culpa! Corrupti quod repudiandae accusantium
    itaque laborum a aut officiis, numquam laudantium maiores cupiditate eaque?
  </p>
</template>

<script>
import napravs from '../data/napravs'
export default {
  data() {
    return {
      napravs
    }
  },
  computed: {
    naprav() {
      return this.napravs.find(item => item.alias === this.$route.params.page)
    }
  }
}
</script>