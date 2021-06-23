<template>
  <div class="row ps-2 pe-2 pb-3">
    <h2 class="text-center mb-4">Готовые решения</h2>
    <div class="col-12">
      <div class="row" id="bgset" v-on:mouseout="outRow">
        <Reshens-item :reshen="reshens[0]" class="col-6 border" />
        <Reshens-item :reshen="reshens[1]" class="col-6 border text-end" />
        <Reshens-item :reshen="reshens[2]" class="col-4 border" />
        <div class="col-4 border" id="backlogotop"></div>
        <Reshens-item :reshen="reshens[3]" class="col-4 border text-end" />
        <Reshens-item :reshen="reshens[4]" class="col-4 border" />
        <div class="col-4 border" id="backlogobot"></div>
        <Reshens-item :reshen="reshens[5]" class="col-4 border text-end" />
        <Reshens-item :reshen="reshens[6]" class="col-6 border" />
        <Reshens-item :reshen="reshens[7]" class="col-6 border text-end" />
      </div>
    </div>
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

<style scoped>
#bgset {
  background: url('/img/index/reshens/circle_00.png') center top no-repeat;
  -webkit-transition: background 0.3s linear;
  -moz-transition: background 0.3s linear;
  -o-transition: background 0.3s linear;
  -ms-transition: background 0.3s linear;
  transition: background 0.3s linear;
}

#backlogotop {
  background: url('/img/index/reshens/center_logo.png') center top no-repeat;
}
#backlogobot {
  background: url('/img/index/reshens/center_logo.png') center bottom no-repeat;
}
</style>