<template lang="html">
    <Panel title="众筹新品" :class="$style.panel">
        <section :class="$style.content">
            <div class="arrow">更多尖货 ></div>
            <Slider :options="options" :items="items" cname="product-slider"/>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t21559/102/59104594/47942/f8d9e459/5af9055dN55aa9554.jpg?width=335&height=421",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t21364/117/63805922/48719/7d9b8fb4/5af9056aN106a173e.jpg?width=335&height=421",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t16717/179/2537323270/43542/a5a5e4c/5af90576Ndba39333.jpg?width=335&height=421",
            }],
            options: {
                slidesPerView: 2.3,
                spaceBetween: 30,
                freeMode: true,
            },
        }
    },
}
</script>

<style lang="scss">
  .product-slider{
    .swiper-container{
      box-sizing: border-box;
      padding: 0 24px;
      .swiper-slide{
        a{
          display: inline-block;
          width: 100%;
          img{
            width: 100%;
            display: block;
            height: 314px;
            border: 1px solid #fafafa;
          }
        }
      }
    }
  }
</style>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    .content{
      padding-bottom: 40px;
      position: relative;
      &>div{
        position: absolute;
        font-size: 28px;
        color: #999;
        right:20px;
        top: -70px;
      }
    }
  }
</style>
