<template lang="html">
    <article class="">
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.sign">
            <ul>
                <li>
                    <p>新手</p>
                </li>
                <li>
                    <p>0</p>
                    <p>钢镚</p>
                </li>
                <li>
                    <button>签到</button>
                </li>
            </ul>
        </section>
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in enters" :key="item.img">
                <router-link :to="{ name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22297/80/283596775/51077/8c003361/5b080d52N14333862.jpg?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t21433/218/283807853/45843/170c9925/5b0808e2N59aee9ec.jpg?width=750&height=400",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t22348/277/278055025/41362/97d2c608/5b0808f6N25f713ae.jpg?width=750&height=400",
            },{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t21904/164/286908241/38611/281d904f/5b08090eN91b5cd99.jpg?width=750&height=400",
            }],
            enters: [{
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t22318/99/279243685/12708/b1e98c82/5b079479Nc3aea2dd.png?width=90&height=90",
                title: "领红包",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t21250/333/257920646/13618/d61f2e32/5b079489Nc22bdecd.png?width=90&height=90",
                title: "领福利",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t21967/161/261734533/13559/9a977165/5b079494Na8af3ac5.png?width=90&height=90",
                title: "领劵",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t21733/194/259135291/14001/c96467e4/5b07949eNdb787303.png?width=90&height=90",
                title: "支付抽奖",
            }, {
                href: "home",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t20530/315/258030039/13697/27444d09/5b0794a6N0f299bee.png?width=90&height=90",
                title: "全部",
            }],
        }
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .slider{
    margin-top: 100px;
    img{
      width: 100%;
    }
  }
  .list{
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a{
      text-decoration: none;
    }
    .item{
      text-align: center;
      img{
        display: inline-block;
        width: 90px;
        height: 90px;
      }
      h4{
        font-size: 26px;
        margin-top: 12px;
        color: #666;
      }
    }
  }
  .sign{
    width: 100%;
    background-color: #fff;
    ul{
        @include list(row);
        height: 130px;
        padding: 0 20px;
        margin: 0 32px;
        box-sizing: border-box;
        align-items: center;
        justify-content: space-between;
        background-color: #fff;
        box-shadow: 0 0 24px 1.5px rgba(101,118,155,.15);
        position: relative;
        z-index: 20;
        border-radius: 4px;
        top: -10px;
        li{
            font-size: 24px;
            color: #fff;
            text-align: center;
            &:nth-child(1) p{
                width: 92px;
                height: 66px;
                line-height: 66px;
                border-radius: 4px;
                background-image: linear-gradient(135deg, #b2b6bf 0%, #4a5662 100%);
                box-shadow: 0 6px 1px 0 rgba(117,125,147,.53);
            }
            &:nth-child(2) p:nth-child(1){
                color: #c4a36c;
                font-size: 36px;
                margin-bottom: 3px;
                font-weight: bold;
                
            }
            &:nth-child(2) p:nth-child(2){
                color: #333;                
            }
            button{
                @include btn($size:24px,$radius:30px);
                width: 140px;
                height: 66px;
                background-image: linear-gradient(135deg, #f2dca3, #a0875e);
                border-color: transparent;
                box-shadow: 0 10px 15px 0 hsla(40,41%,61%,.41);

            }
        }
    }
  }
</style>
