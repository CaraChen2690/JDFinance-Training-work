<template lang="html">
    <Panel title="有车有钱" :class="$style.panel">
        <ul :class="$style.carAndMoney">
            <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t18319/288/2020359902/20747/e4c1e6d4/5ae28f3bN8d2fabad.png?width=375&height=233" alt=""></li>
            <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233" alt=""></li>
        </ul>
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide >
                <ul :class="$style.selection">
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90" alt="">
                        <p>旅游</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90" alt="">
                        <p>医美</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88" alt="">
                        <p>房抵贷</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90" alt="">
                        <p>驾校</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88" alt="">
                        <p>分期用</p>
                    </li>
                </ul>  
            </swiper-slide>
            <swiper-slide >
                <ul :class="$style.selection">
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16183/231/1309653281/4671/3ace8435/5a4f27d0N9e3df1d5.png?width=90&height=90" alt="">
                        <p>教育</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t15955/206/1280935063/4274/6204375a/5a4f2801N015920c5.png?width=90&height=90" alt="">
                        <p>车险</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t15451/2/1424737894/3801/e7844c76/5a4f2823Ne430c735.png?width=88&height=88" alt="">
                        <p>家庭</p>
                    </li>
                    <li :class="$style.item">
                        <img src="//img12.360buyimg.com/jrpmobile/jfs/t15922/204/1330308267/4745/e0cae4a0/5a4f2836Nd00354cb.png?width=90&height=90" alt="">
                        <p>租房</p>
                    </li>
                </ul>  
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
      </swiper>
        
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import { swiper, swiperSlide } from "vue-awesome-swiper"
export default {
    components: {
        Panel,
        swiper,
        swiperSlide
    },
    data(){
        return{
            options:{
                pagination: {
                    el: ".swiper-pagination",
                },
                notNextTick: false,
            }
        }
    },
}
</script>

<style lang="scss">
  .swiper-slide{
    margin-bottom: 20px;
  }
</style>
<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    .carAndMoney{
      @include flex(row);
      padding-bottom: 40px;
      li{
        width: 50%;
        img{
          width: 100%;
          height: auto;
        }
      }
    }
    .selection{
      @include flex(row);
      box-sizing: border-box;
      padding-top: 40px;
      padding-bottom: 10px;
      .item{
        width: 20%;
        text-align: center;
        img{
          width: 90px;
          height: 90px;
        }
        p{
          font-size: 26px;
          color: #666;
          margin-top: 12px;
        }
      }
    }
  }
</style>
