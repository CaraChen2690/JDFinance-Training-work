<template lang="html">
    <Panel title="保险保障" :class="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.theme">
                <p :class="$style.itro">今日推荐</p>
                <p :class="$style.money">100万</p>
                <p :class="$style.introduce">账户安全险</p>
                <button>免费领取</button>
            </li>
            <li :class="$style.list">
                <ul>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8881/304/1359242815/2540/5ef07179/59b90050N62f41061.png?width=56&height=56" alt="">
                      <p>车险</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9040/57/2313007861/3024/82c36c44/59ca556eNb605e901.png?width=56&height=56" alt="">
                      <p>人寿</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9283/283/1383600733/3117/82a51164/59b900cfNe88db318.png?width=56&height=56" alt="">
                      <p>意外</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8929/33/1393593833/1749/1e115bd7/59b900e6N73c7b311.png?width=56&height=56" alt="">
                      <p>财产</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8902/275/1411242449/2807/a2cc902a/59b90111N4e88098c.png?width=56&height=56" alt="">
                      <p>健康</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8962/170/1384497943/2594/aa2a2ad9/59b9011bNf3b01bea.png?width=56&height=56" alt="">
                      <p>旅行</p>
                    </li>
                </ul>
            </li>
        </ul>
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t18631/176/1296661704/41624/f193c3f6/5ac2e521N06980907.png?width=750&height=200" alt="">
        <h6>热销保险</h6>
        <Slider :options="options" :items="items" cname="product-slider"/>
        <img src="https://img12.360buyimg.com/jrpmobile/jfs/t19756/137/1902911799/17823/e19ffe7b/5add9511Nf6984e89.jpg?width=750&height=200" alt="">
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"

export default {
    components: {
        Panel,
        Slider
    },
    data() {
        return {
            items: [{
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t9697/338/291348712/12737/27e1204/59cb6304Naef85042.jpg?width=210&height=260",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t10360/347/311063647/10881/14a5cd40/59cb632fNcac82571.jpg?width=210&height=260",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t13927/226/2090083878/14208/2746192a/5a31dde6Nbba7f26c.png?width=210&height=260",
            }, {
                href: "home",
                src: "//img12.360buyimg.com/jrpmobile/jfs/t9703/119/296348375/11253/b9bc3ce7/59cb637dNf25b0dff.jpg?width=210&height=260",
            }],
            options: {
                slidesPerView: 2.5,
                spaceBetween: 15,
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
        @include list(row);
        width: 100%;
        // height: 300px;
        flex-wrap: nowrap;
        .theme{
            width: 210px;
            height: 260px;
            margin: 0 16px 16px 30px;
            text-align: center;
            box-shadow: 0 0 26px 1px rgba(101,118,155,.15);
            .itro{
                width: 96px;
                height: 32px;
                line-height: 32px;
                font-size: 24px;
                background: #000;
                color: #fff;
                padding: 0 12px;
            }
            .money{
                font-size: 50px;
                color: #1bd5c7;
                height: 61px;
                line-height: 61px;
                margin: 35px 0 4px;
            }
            .introduce{
                font-size: 24px;
                height: 34px;
                line-height: 34px;
                margin-bottom: 24px;
            }
            button{
                @include btn($size:24px,$color:#fff,$bgcolor:rgb(27, 213, 199),$padding:12px,$radius:30px);
                width: 140px;
                height: 50px;
            }
        
        }
        .list{
            ul{
                @include list(row);
                width: 354px;
                height: 260px;
                margin-right: 30px;
                text-align: center;
                font-size: 24px;
                box-shadow: 0 0 26px 1px rgba(101,118,155,.15);
                li{
                  width: 115px;
                  height: 130px;
                  img{
                    margin: 20px 31px 2px;
                    width: 56px;
                    height: 56px;
                  }
                  p{
                    width: 94px;
                    padding: 0 12px;
                    text-overflow: ellipsis;
                    overflow: hidden;
                    white-space: nowrap;
                  }
                }

            }
        }
    }
    >img{
        width: 100%;
        margin-top: 15px;
    }
    >h6{
        height: 100px;
        line-height: 100px;
        font-size: 28px;
        margin-left: 30px;
    }
}
</style>
