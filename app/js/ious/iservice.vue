<template lang="html">
    <Panel title="白条服务" :class="$style.panel">
        <ul :class="$style.content">
          <li><img src="//m.jr.jd.com/vip/borrowMoney/widget/bannerAndCar/i/whiteCard.png" alt=""></li>
          <li>
            <img src="//m.jr.jd.com/vip/borrowMoney/widget/bannerAndCar/i/whiteCircle.png" alt="">
            <p :class="$style.txt1">89.3</p>
            <p :class="$style.txt2">小白信用</p>
            <p :class="$style.txt3">立即开通</p>
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
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    .content{
      @include flex(row);
      padding-bottom: 40px;
      li{
        &:nth-child(1){
          width: 63.5%;
          padding-right: 13px;
          box-sizing: border-box;
        }
        &:nth-child(2){
          width: 36%;
          position: relative;
          padding-right: 13px;
          box-sizing: border-box;
          p{
            color: #fff;
            position: absolute;
            right: 0;
            left: 0;
            bottom: auto;
            text-align: center;
          }
          .txt1{
            font-size: 36.5px;
            top: 30%;
            line-height: 47px;
          }
          .txt2{
            font-size: 24px;
            line-height: 26px;
            color: #ffeac9;
            top: 47%;
          }
          .txt3{
            color: #ae8339;
            font-size: 24px;
            line-height: 26px;
            top: 66.5%;
            padding-right: 6%;
            box-sizing: border-box;
          }
        }
        img{
          width: 100%;
          height: auto;
        }
      }
    }
  }
</style>
