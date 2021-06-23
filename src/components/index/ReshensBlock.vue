<template>
  <div class="row ps-2 pe-2 pb-3">
    <h2 class="text-center mb-4">Готовые решения</h2>
    <div class="col-12">
      <div class="row" id="bgset" @mouseout="resetSector" ref="sector">
        <Reshens-item
          :reshen="reshens[0]"
          class="col-6"
          @mouseover="setSector(1)"
        />
        <Reshens-item
          :reshen="reshens[1]"
          class="col-6 text-end"
          @mouseover="setSector(2)"
        />
        <Reshens-item
          :reshen="reshens[2]"
          class="col-4"
          @mouseover="setSector(3)"
        />
        <div class="col-4" id="backlogotop">
          <router-link
            to="/abouts/deyatelnost"
            aria-label="О компании"
            class="d-block w-100 h-100"
          ></router-link>
        </div>
        <Reshens-item
          :reshen="reshens[3]"
          class="col-4 text-end"
          @mouseover="setSector(4)"
        />
        <Reshens-item
          :reshen="reshens[4]"
          class="col-4"
          @mouseover="setSector(5)"
        />
        <div class="col-4" id="backlogobot">
          <router-link
            to="/abouts/deyatelnost"
            aria-label="О компании"
            class="d-block w-100 h-100"
          ></router-link>
        </div>
        <Reshens-item
          :reshen="reshens[5]"
          class="col-4 text-end"
          @mouseover="setSector(6)"
        />
        <Reshens-item
          :reshen="reshens[6]"
          class="col-6"
          @mouseover="setSector(7)"
        />
        <Reshens-item
          :reshen="reshens[7]"
          class="col-6 text-end"
          @mouseover="setSector(8)"
        />
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
  },
  methods: {
    setSector(secNum) {
      this.$refs.sector.style =
        "background: url('/img/index/reshens/circle_0" +
        secNum +
        ".png') center top no-repeat;"
    },
    resetSector() {
      this.$refs.sector.style =
        "background: url('/img/index/reshens/circle_00.png') center top no-repeat;"
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