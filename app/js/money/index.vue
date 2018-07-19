<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Mactivity></Mactivity>
        <Chest></Chest>
        <Crowd></Crowd>
        <Minsurance></Minsurance>
        <Mious></Mious>
        <Stock></Stock>
        <Recommend></Recommend>
        <Footor cname="mfooter"/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./mslider.vue"
import Mactivity from "./mactivity.vue"
import Chest from "./chest.vue"
import Crowd from "./crowd.vue"
import Minsurance from "./minsurance.vue"
import Mious from "./mious.vue"
import Stock from "./stock.vue"
import Recommend from "./recommend.vue"
export default {
    components: {
        Heador,
        Slider,
        Mactivity,
        Chest,
        Crowd,
        Minsurance,
        Mious,
        Stock,
        Recommend,
        Footor,
        Navbar,
    },
}
</script>

<style lang="scss">
  .mfooter{
    margin-top: 0!important;
    ul{
      li:first-child{
        display: none;
      }
    }
  }
</style>
