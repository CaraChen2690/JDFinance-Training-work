<template lang="html">
    <Panel title="京东众筹" :class="$style.panel">
        <a href="">好生活 享品质></a>
        <ul :class="$style.content">
            <li :class="$style.theme">
                <p :class="$style.itro">今日推荐</p>
                <p :class="$style.money">0.01元</p>
                <p :class="$style.introduce">抢好物</p>
                <button>立即抢购</button>
            </li>
            <li :class="$style.list">
                <ul>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9739/355/2223965438/3092/b3cc4062/59f2fef3Nc2363e64.png?width=56&height=56" alt="">
                      <p>京东出众</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10882/187/2325566882/2968/e64c911c/59f2ff2cNd85eb522.png?width=56&height=56" alt="">
                      <p>手机优惠</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t11674/229/560588342/2307/d88f9fd7/59f2ff5eNcac8d195.png?width=56&height=56" alt="">
                      <p>领神劵</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t10018/213/2260133396/2902/107476f0/59f2ff70N35c5d0bb.png?width=56&height=56" alt="">
                      <p>智能首发</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t7552/255/3352153359/2695/fc610922/59f2ff88N95232a40.png?width=56&height=56" alt="">
                      <p>舌尖美食</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9523/348/2258037555/2792/9e8e1a80/59f2ff9fNf9648450.png?width=56&height=56" alt="">
                      <p>轻时尚</p>
                    </li>
                </ul>
            </li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"

export default {
    components: {
        Panel,
    },
    data() {
        return {

        }
    },
}
</script>

<style lang="scss" module>
@import "../../css/element.scss";
.panel{
    @include panel;
    position: relative;
    a{
      font-size: 24px;
      color: #999;
      text-decoration: none;
      position: absolute;
      top: 45px;
      right: 15px;
    }
    .content{
        @include list(row);
        width: 100%;
        height: 300px;
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
                  width: 118px;
                  height: 130px;
                  img{
                    margin: 20px 31px 2px;
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
}
</style>
