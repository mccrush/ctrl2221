<template>
  <div class="row ps-2 pe-2 pb-3">
    <h2 class="text-center mb-4">Готовые решения</h2>
    <Reshens-item v-for="reshen in reshens" :key="reshen.id" :reshen="reshen" />
  </div>
</template>

<script>
import reshens from '@/data/reshens'
import ReshensItem from '@/components/index/ReshensItem'

export default {
  components: {
    ReshensItem
  },
  data() {
    return {
      reshens
    }
  }
}
</script>