<template>
  <div class="row ps-2 pe-2">
    <div class="col-12">
      <h1>{{ page.title }}</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet itaque
        eaque eos cumque libero excepturi culpa! Corrupti quod repudiandae
        accusantium itaque laborum a aut officiis, numquam laudantium maiores
        cupiditate eaque?
      </p>
      <ul v-if="$route.params.razdel === 'napravs'">
        <li v-for="item in napravs_vidFiltered" :key="item.id">
          <router-link :to="'/napravs_vid/' + item.alias">{{
            item.title
          }}</router-link>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
import napravs from '@/data/napravs'
import napravs_vid from '@/data/napravs_vid'
import abouts from '@/data/abouts'
export default {
  data() {
    return {
      napravs,
      napravs_vid,
      abouts
    }
  },
  computed: {
    page() {
      if (this.$route.params.razdel === 'napravs') {
        return this.napravs.find(page => page.alias === this.$route.params.page)
      } else if (this.$route.params.razdel === 'napravs_vid') {
        return (
          this.napravs_vid.find(
            page => page.alias === this.$route.params.page
          ) || {
            title: 'Ошибка 404. Страница не найдена'
          }
        )
      } else if (this.$route.params.razdel === 'abouts') {
        return (
          this.abouts.find(page => page.alias === this.$route.params.page) || {
            title: 'Ошибка 404. Страница не найдена'
          }
        )
      }
    },
    napravs_vidFiltered() {
      return this.napravs_vid.filter(
        item => item.naprav === this.$route.params.page
      )
    }
  }
}
</script>

<style scoped>
a:hover,
a:active {
  text-decoration: none;
}
</style>