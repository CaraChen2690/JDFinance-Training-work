<template lang="html">
    <Panel title="轮播图" :class="$style.panel">
        <section :class="$style.content">
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t19783/355/938803703/27459/b16b944a/5ab0e9d7Na5432129.png?width=1863&height=285" alt="">
            <div :class="$style.card">
                <!-- <div>
                    <img src="//m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/goldCard.png" alt=""> -->
                    <p :class="$style.txt1">最高可借</p>
                    <p :class="$style.txt2">¥<span>300,000</span></p>
                    <p :class="$style.txt3">申请开通</p>
                <!-- </div> -->
            </div>
            <Slider :items="items" cname="borrow-slider"></Slider>
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
                href: "ious",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t16612/150/2618203774/18622/7b19c9e9/5b04ce9eN39dd756a.png?width=690&height=154",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t20047/16/651274638/48561/ae45dcc1/5b04ceb5N04d79ba9.png?width=690&height=154",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t20047/16/651274638/48561/ae45dcc1/5b04ceb5N04d79ba9.png?width=690&height=154",
            }],
        }
    },
}
</script>

<style lang="scss">
.borrow-slider{
    .swiper-slide{
        width: 100%;
        padding: 0 26px;
        box-sizing: border-box;
        img{
            width: 100%;
            height: auto;
            padding: 0 26px;
            margin-bottom: 26px;
            box-sizing: border-box;
        }
    }
}
</style>

<style lang="scss" module>
    @import "../../css/element.scss";
    .panel{
        @include panel;
        margin-top: 100px!important;
        >h4{
          display: none;
        }
        .content{
            background: url(//m.jr.jd.com/vip/borrowMoney/css/i/bj.png) 0 0 no-repeat;
            background-size: 100% auto;
            >img{
                width: 100%;
                height: auto;
                // padding: 0 26px;
                // margin-bottom: 26px;
                box-sizing: border-box;
            }
            .card{
                width: 100%;
                height: 441px;
                padding: 47px 26px;
                box-sizing: border-box;
                background: url(//m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/goldCard.png) center center/100% 100% content-box no-repeat;
                // div{
                //     position: relative;
                //     color: #fff;
                //     img{
                //         width: 100%;
                //     }
                // }
                p{
                    margin-left: 10%;
                    color: #fff;
                }
                .txt1{
                       margin-top: 8%;
                       margin-bottom: 2%;
                       font-size: 28px;
                }
                .txt2{
                    font-size: 52px;
                    span{
                        font-size: 75px;
                    }
                }
                .txt3{
                    font-size: 24.5px;
                    width: 180px;
                    height: 57px;
                    line-height: 57px;
                    text-align: center;
                    margin-top: 3%;
                    background: url(//m.jr.jd.com/vip/borrowMoney/widget/jdGold/i/btnBj.png) 0 0/100% 100% no-repeat;
                }
            }
        }
    }
</style>
