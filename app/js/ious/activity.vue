<template lang="html">
    <Panel title="精品活动" :class="$style.panel">
        <ul :class="$style.content">
          <li><img src="//img12.360buyimg.com/jrpmobile/jfs/t20620/150/260030723/15028/e868cb0d/5b079963N65616e9a.png?width=376&height=264" alt=""></li>
          <li>
            <img src="//img12.360buyimg.com/jrpmobile/jfs/t18901/214/2385188321/64672/bf6f1441/5af16613N5423430b.png?width=376&height=264" alt="">
          </li>
        </ul>
        <img src="//img12.360buyimg.com/jrpmobile/jfs/t16675/365/91110617/54621/c0042c09/5a5c87faNd161d42e.png?width=730&height=264" alt="">
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
      li{
        width: 50%;
        img{
          width: 100%;
          height: auto;
        }
      }
    }
    >img{
      width: 100%;
      height: auto;
    }
  }
</style>
