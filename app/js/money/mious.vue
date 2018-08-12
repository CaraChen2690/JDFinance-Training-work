<template lang="html">
    <Panel title="白条" :class="$style.panel">
        <a href="">年轻不留白></a>
        <ul :class="$style.content">
            <li :class="$style.theme">
                <p :class="$style.money">89.3</p>
                <p :class="$style.introduce">小白信用</p>
                <button>预估分数</button>
            </li>
            <li :class="$style.list">
                <ul>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8803/130/802395570/1891/103bedf1/59af980eN987fd5c2.png?width=56&height=56" alt="">
                      <p>白条</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9373/154/878445473/2758/410dc92d/59b901f5Nc93edaac.png?width=56&height=56" alt="">
                      <p>还款</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t9391/169/1385525558/2762/2d29f1d5/59b90214N4f745107.png?width=56&height=56" alt="">
                      <p>1元抢券</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t7246/167/3036813324/1578/d4ae001e/59b90228Nd61b6465.png?width=56&height=56" alt="">
                      <p>小白卡</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t8422/203/1374629409/2823/430e740d/59b90230N09140aba.png?width=56&height=56" alt="">
                      <p>金条</p>
                    </li>
                    <li>
                      <img src="https://img12.360buyimg.com/jrpmobile/jfs/t7618/313/3082994165/3330/e1692006/59b90247Nac3c9ebe.png?width=56&height=56" alt="">
                      <p>校园</p>
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
            background: url(https://m.jr.jd.com/vip/borrowMoney/widget/bannerAndCar/i/whiteCircle.png) center center/110% no-repeat;
            .money{
                font-size: 36px;
                color: #fff;
                height: 61px;
                line-height: 61px;
                margin: 45px 0 4px;
            }
            .introduce{
                font-size: 24px;
                height: 34px;
                line-height: 34px;
                margin-bottom: 24px;
                color: #fff;
            }
            button{
                @include btn($size:24px,$color:#c4a36c,$bgcolor:#fff,$padding:12px,$radius:30px);
                width: 140px;
                height: 40px;
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
}
</style>
