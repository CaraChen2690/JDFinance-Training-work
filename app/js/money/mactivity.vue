<template lang="html">
    <article class="">
        <section :class="$style.discounts">
            <div :class="$style.rate">
                <p><span>11.7</span>%</p>
                <p>历史年化收益率</p>
                <p>签到领红包</p>
            </div>
            <section class="vslider">
                <swiper :options="options" :not-next-tick="options.notNextTick">
                    <swiper-slide v-for="item in items" :key="item.href">
                        <img :src="item.src" alt="">
                        <p>{{ item.text }}</p>
                    </swiper-slide>
                </swiper>
            </section>
        </section>
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t20161/67/373823770/37378/799b3d4a/5b0baad9N8f198709.png?width=750&height=260" alt="" :class="$style.activeImg">
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9799/266/1810669512/19559/34bdcf8/59e81a59Nf5a858a9.png?width=750&height=240" alt="" :class="$style.activeImg">
    </article>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"
export default {
    components: {
        swiper,
        swiperSlide,
    },
    data() {
        return {
            items:[{
                src: "https://img12.360buyimg.com/jrpmobile/jfs/t16945/128/2663814248/11446/a6569a02/5b06c634Na91714a1.jpg?width=160&height=160",
                text: "宝丽来超短焦巨屏电视 4折秒杀",
            },{
                src: "https://img12.360buyimg.com/jrpmobile/jfs/t20722/67/251648719/7833/ad5b61e6/5b06c605N0c399ef0.jpg?width=160&height=160",
                text: "咕咚智能跑鞋  限时立省320元",
            },{
                src: "https://img12.360buyimg.com/jrpmobile/jfs/t18832/140/2659708740/6054/c2e483b5/5b06c663Nbffe28bf.jpg?width=160&height=160",
                text: "多功能灭蚊灯 赠驱蚊手环",
            },{
                src: "https://img12.360buyimg.com/jrpmobile/jfs/t22321/48/244953432/9035/d805b6e4/5b06c653N21873ed9.jpg?width=160&height=160",
                text: "智能颈椎按摩仪 直降200元",
            },{
                src: "https://img12.360buyimg.com/jrpmobile/jfs/t18745/69/2678928044/3539/d31d6d55/5b06c621Nde822a76.jpg?width=160&height=160",
                text: "智能睡眠机器人 众筹价立省500元",
            }],
            options: {
                autoplay: true,
                delay: 3000,
                loop: true,
                direction: "vertical",
                notNextTick: false,
            },
        }
    },
}
</script>

<style lang="scss">
    .vslider{
        .swiper-container{
            background-image: linear-gradient(90deg,#6c8bff,#374dde);
            margin: 0 50px 0 16px;
            width: 80%;
            height: 200px;
            box-sizing: border-box;
            .swiper-slide{
                vertical-align: top;
                img{
                    float: left;
                    margin: 20px 20px 0 20px;
                    width: 160px;
                    height: 160px;
                }
                p{
                    float: left;
                    font-size: 24px;
                    width: 44%;
                    height: 28px;
                    line-height: 28px;
                    color: #fff;
                    margin-top: 20px;
                }
            }
        }
    } 
        
</style>
<style lang="scss" module>
@import "../../css/element.scss";
.discounts{
    @include list(row);
    flex-wrap: nowrap;
    background-color: #fff;
    width: 100%;
    height: 200px;
    overflow: hidden;
    padding: 30px;
    .rate{
        color: #fff;
        background-image: linear-gradient(#ec7225, #f24d31);
        width: 20%;
        padding: 25px 38px 24px 24px;
        p{
            font-size: 24px;
            text-overflow: ellipsis;
            white-space: nowrap;
            overflow: hidden;
            box-sizing: border-box;
            margin-bottom: 15px;
            span{
                font-size: 50px;
                height: 70px;
                line-height: 58px;
            }
        }
    }
 }
.activeImg{
    width: 100%;
    margin-top: 40px;
}
</style>
