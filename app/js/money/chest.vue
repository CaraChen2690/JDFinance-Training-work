<template lang="html">
    <Panel title="小金库" :class="$style.panel">
        <section :class="$style.gift">
            <div>
                <p :class="$style.benifit"><span>4.3040</span>%</p>
                <p :class="$style.title">七日年化收益</p>
                <p :class="$style.desc">支付/缴费/优质理财/大额理财</p>
                <button :class="$style.btn">开启送礼包</button>
            </div>
        </section>
        <section :class="$style.funds">
            <h6>稳健灵活 定期理财</h6>
            <div class="fundsslider">
                <swiper :options="options" :not-next-tick="options.notNextTick">
                    <swiper-slide v-for="item in items" :key="item.name">
                        <p class="name">{{ item.name }}</p>
                        <p class="intro">{{ item.intro }}</p>
                        <p class="rate"> {{ item.rate }}<span>%</span></p>
                        <p class="introduce"> {{item.introduce}} </p>
                    </swiper-slide>
                </swiper>
            </div>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import { swiper, swiperSlide } from "vue-awesome-swiper"
export default {
    components: {
        Panel,
        swiper,
        swiperSlide,
    },
    data() {
        return {
            options: {
                slidesPerView: 2.7,
                spaceBetween: 16,
                freeMode: true,
                notNextTick: false,
                pagination: {
                        el: ".swiper-pagination",
                    },
            },
            items: [{
                name: "年年盈",
                intro: "金融专享",
                rate: "5.80",
                introduce: "近七日年化收益率",
            }, {
                name: "周期盈",
                intro: "理财优选",
                rate: "5.04",
                introduce: "近七日年化收益率",
            }, {
                name: "双年盈",
                intro: "2年可赎回",
                rate: "6.00",
                introduce: "历史年化投资收益率",
            }, {
                name: "随享盈",
                intro: "质押贷款",
                rate: "5.50",
                introduce: "历史年化结算收益率",
            }],
        }
    },
}
</script>

<style lang="scss">
  .fundsslider{
    .swiper-container{
      width: 100%;
      box-sizing: border-box;
      height: 300px;
      padding: 0 24px;
      .swiper-slide{
          height: 260px;
          padding: 0 30px;
          box-sizing: border-box;
          box-shadow: 0 0 24px 1.5px rgba(101,118,155,.15);
          .name{
            font-size: 32px;
            margin: 38px auto 10px;
            height: 46px;
            line-height: 46px;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
          }
          .intro{
            min-width: 100px;
            font-size: 24px;
            height: 32px;
            line-height: 32px;
            background-image: linear-gradient(#5e8fff,#2f6fff);
            color: #fff;
            display: inline-block;
            border-radius: 22px;
            text-align: center;
          }
          .rate{
            font-size: 50px;
            height: 60px;
            line-height: 60px;
            color: #ff281e;
            white-space: nowrap;
            text-overflow: ellipsis;
            overflow: hidden;
            span{
              font-size: 24px;
            }
          }
          .introduce{
            font-size: 24px;
            height: 28px;
            line-height: 28px;
            color: #999;
            margin-top: 8px;
          }
        }  
      }
    }
</style>
<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    .gift{
      width: 100%;
      min-height: 200px;
      padding: 0 30px;
      box-sizing: border-box;
      div{
        height: 200px;
        background: url(https://m.jr.jd.com/spe/qyy/hzq/445b538c873a5bffc189ad117298eec4.png) 50%/cover  no-repeat;
        color: #fff;
        font-size: 24px;
        border-radius: 4px;
        padding-left: 28px;
        overflow: hidden;
        position: relative;
        .benifit{
            height: 72px;
            letter-spacing: 0.00496px;
            margin-top: 24px;
            width: 280px;
            span{
              font-size: 60px;
              font-weight: bold;
            }

        }
        .title{
          height: 34px;
          line-height: 34px;
          margin: 8px 0 4px;
        }
        .desc{
          height: 34px;
          line-height: 34px;
          opacity: .6;
        }
        .btn{
          width: 332px;
          height: 200px;
          line-height: 200px;
          position: absolute;
          top: 0;
          right: 0;
          background: url(https://m.jr.jd.com/spe/qyy/hzq/ac3595803ef2dfd8530f13be01cbdead.png) 50%/cover  no-repeat;
          text-aligh: center;
          font-size: 24px;
          color: #fff;
          border: none;
        }
      }
    }
    .funds{
      h6{
        height: 100px;
        line-height: 100px;
        font-size: 28px;
        margin: 0 30px;
      }
    }
  }
</style>
