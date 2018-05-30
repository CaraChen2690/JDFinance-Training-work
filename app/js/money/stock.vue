<template lang="html">
    <Panel title="白条" :class="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.left">
                <img src="https://img30.360buyimg.com/jr_image/jfs/t5848/216/253631918/136369/1894b4a7/591e5567Ncfb35e99.jpg" alt="">
                <p :class="$style.benifit">375.23<span>%</span></p>
                <p :class="$style.title">累计收集排行榜</p>
                <p :class="$style.desc">
                    <span>牛人</span>
                    zangyn
                </p>
                <img src="https://m.jr.jd.com/spe/qyy/hzq/src/static/images/go_btn.png" alt="">
            </li>
          <li :class="$style.right">
              <p :class="$style.benifit">竞猜大盘涨跌</p>
              <p :class="$style.title">赢500钢镚</p>
              <p :class="$style.desc">立即前往</p>
              <img src="https://m.jr.jd.com/spe/qyy/hzq/src/static/images/go_btn.png" alt="">
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
    .content{
        @include list(row);
        width: 100%;
        height: 250px;
        padding: 0 30px;
        box-sizing: border-box;
        justify-content: space-between;
        li{
            width: 49%;
            height: 200px;
        }
        .left{
            background: url(https://img12.360buyimg.com/jrpmobile/jfs/t8767/137/977390432/7475/e5acd251/59ba3a31Ncbd06cac.jpg?width=335&height=200) 0 0/100% 100% no-repeat;
            position: relative;
            color: #fff;
            img:nth-child(1){
                width: 90px;
                height: 90px;
                border-radius: 50%;
                position: absolute;
                top: 30px;
                left: 20px;
            }
            .benifit{
                font-size: 36px;
                position: absolute;
                height: 52px;
                line-height: 52px;
                top: 23px;
                left: 130px;
                span{
                    font-size: 24px;
                }
            }
            .title{
                font-size: 24px;
                height: 34px;
                line-height: 34px;
                position: absolute;
                top: 78px;
                left: 130px;
            }
            .desc{
                font-size: 24px;
                position: absolute;
                bottom: 30px;
                right: 84px;
                span{
                    width: 60px;
                    height: 30px;
                    line-height: 30px;
                    text-align: center;
                    display: inline-block;
                    background-image: linear-gradient(-90deg,#fd5737,#ec3038);
                }
            }
            img{
                width: 50px;
                height: 50px;
                position: absolute;
                bottom: 20px;
                right: 20px;
            }

        }
        .right{
            background: url(https://img12.360buyimg.com/jrpmobile/jfs/t15661/192/2386880166/5534/2d3f9dfd/5aa7310bN2f099f7a.jpg?width=335&height=200) 0 0/100% 100% no-repeat;
            position: relative;
            color: #fff;
            .benifit{
                font-size: 36px;
                position: absolute;
                height: 52px;
                line-height: 52px;
                top: 26px;
                left: 38px;
            }
            .title{
                font-size: 24px;
                height: 34px;
                line-height: 34px;
                position: absolute;
                top: 78px;
                left: 38px;
            }
            .desc{
                font-size: 24px;
                position: absolute;
                bottom: 30px;
                right: 84px;
            }
            img{
                width: 50px;
                height: 50px;
                position: absolute;
                bottom: 20px;
                right: 20px;
            }
        }
    }
}
</style>
