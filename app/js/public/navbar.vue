<template lang="html">
    <Panel title="导航条" :class="$style.panel">
        <ul :class="$style.content">
            <li>
                <router-link :to="{ name: 'home'}">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t17587/158/1300523690/1908/eabacaac/5ac4850bNdf876dd8.png?width=60&height=60" alt="">
                    <p>首页</p>
                </router-link>
            </li>
            <li>
                <router-link :to="{ name: 'money'}">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t7690/252/3621724688/1715/757a3ca1/59e9d81bN27304850.png?width=60&height=60" alt="">
                    <p>赚钱</p>
                </router-link>
            </li>
            <li>
                <router-link :to="{ name: 'home'}">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t11653/76/201131398/1192/bf1b2852/59e9d7f3N5f691137.png?width=60&height=60" alt="">
                    <p>借钱</p>
                </router-link>
            </li>
            <li>
                <router-link :to="{ name: 'home'}">
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t10897/141/1894216742/2046/ad0e8dc1/59e9d7feNaa5dd2fd.png?width=60&height=60" alt="">
                    <p>金融会员</p>
                </router-link>
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
    position: fixed;
    left:0;
    right: 0;
    bottom: 0;
    height: 100px;
    margin: 0;
    z-index: 100;
    >h4{
      display: none;
    }
    .content{
      @include flex(row);
      justify-content: space-around;
      li{
        text-align: center;
        a{
          text-decoration: none;
        }
        img{
          width: 44px;
          height: 44px;
          display: inline-block;
          margin: 12px auto 6px;
        }
        p{
          font-size: 22px;
          color: #656565;
        }
      }
    }
  }
</style>
