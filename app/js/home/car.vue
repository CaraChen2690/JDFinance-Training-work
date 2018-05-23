<template lang="html">
    <Panel title="有车有钱" :class="$style.panel">
        <ul :class="$style.carAndMoney">
          <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t18319/288/2020359902/20747/e4c1e6d4/5ae28f3bN8d2fabad.png?width=375&height=233" alt=""></li>
          <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t14215/140/1757206721/24186/81b4e53c/5a56c877Nee6cfc4d.jpg?width=375&height=233" alt=""></li>
        </ul>
        <ul :class="$style.content">
            <li :class="$style.item">
                <img src="https://img12.360buyimg.com/jrpmobile/jfs/t12799/50/704102454/5247/19eac80a/5a4f2622Nc4aca701.png?width=90&height=90" alt="">
                <p>旅游</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t16033/196/1306232362/4705/4c678227/5a4f265bN66ef5ae8.png?width=90&height=90" alt="">
                <p>医美</p>
            </li>
            <li :class="$style.item">
                <img src="https://img12.360buyimg.com/jrpmobile/jfs/t13051/63/2559290659/4702/e4068917/5a4f2693N937f1905.png?width=88&height=88" alt="">
                <p>房抵贷</p>
            </li>
            <li :class="$style.item">
                <img src="https://img12.360buyimg.com/jrpmobile/jfs/t15133/16/1440686097/5786/1b038e03/5a4f26bfN03ed1f66.png?width=90&height=90" alt="">
                <p>驾校</p>
            </li>
            <li :class="$style.item">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t14896/125/1435676873/3668/a8b392f7/5a4f26edN6cdfda66.png?width=88&height=88" alt="">
                <p>分期用</p>
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
    .content{
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
