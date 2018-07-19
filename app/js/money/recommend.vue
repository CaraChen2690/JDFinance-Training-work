<template lang="html">
    <Panel title="特色推荐" :class="$style.panel">
        <ul :class="$style.content">
            <li :class="$style.product" v-for="product in products" :key="product.title">
                <img :src="product.src" alt="">
                <p :class="$style.title">{{ product.title }}</p>
                <p :class="$style.price"><span>{{ product.price }}</span>起</p>
                <article>
                    <div :class="$style.wrapper">
                        <div :class="$style.inner" :style="{width:product.progress+'%'}"></div>
                    </div>
                    <p>{{ product.progress }}%</p>
                </article>
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
            products: [{
                src: "http://img30.360buyimg.com/cf/jfs/t19174/162/1816301002/15585/886be68f/5ad86bf9N20839b2b.png",
                title: "2345章鱼星球八核私有云盘",
                price: "1.00",
                progress: 648,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t21715/307/161930913/37017/45207d9/5affd1a6N4277aaa3.jpg",
                title: "骑骋V米轻量级折叠智能电动车",
                price: "1.00",
                progress: 386,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t18376/175/2554556538/11164/66de5e11/5afbcd11Nf52992a6.jpg",
                title: "咕咚智能跑鞋10K",
                price: "179.00",
                progress: 718,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t17143/85/2578960278/14159/78321af5/5affa11aNf3847350.jpg",
                title: "热血V8微型电单车",
                price: "1.00",
                progress: 354,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t21550/155/347945173/53440/53c2ee50/5b0b7ea5Nbbf051ff.jpg",
                title: "海神 全伴侣科学教育版",
                price: "189.00",
                progress: 95,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t21664/66/104332621/63461/8034512c/5afc2ac8Nd601ea98.png",
                title: "新境界 更多彩·骏派CX65",
                price: "1.00",
                progress: 243,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t21226/276/389169737/65406/752a3c16/5b0bb9b7N25a30e47.jpg",
                title: "手机膜法传奇-1擦秒变新机",
                price: "49.00",
                progress: 174,
            }, {
                src: "http://img30.360buyimg.com/cf/jfs/t19498/20/2017170636/8628/b1f0c563/5ae2ed00Na1fa7270.jpg",
                title: "夏日速干冰爽运动短裤",
                price: "19.00",
                progress: 598,
            }, ],
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
        background-color: #f5f5f5;
        .product:nth-child(2n){
            margin-right: 0;
        }
        .product{
            width: 49%;
            height: 413px;
            box-sizing: border-box;
            text-align: center;
            margin: 0 8px 8px 0;
            background-color: #fff;
            >img{
                width: 228px;
                height: 179px;
                margin-top: 44px;
            }
            .title{
                font-family: PingFangSC-Regular;
                font-size: 30px;
                margin: 22px 0;
                height: 42px;
                line-height: 42px;
                padding-left: 30px;
                white-space: nowrap;
                text-overflow: ellipsis;
                overflow: hidden;
            }
            .price{

                font-size: 24px;

                height: 34px;
                padding-left: 30px;
                line-height: 34px;
                color: #999;
                margin-bottom: 14px;
                text-align: left;
                span{
                    font-family: DIN-Bold;
                    font-size: 32px;
                    color: #ff9a1c;
                    margin-right: 5px;
                    &:before{
                        content:"￥";
                        color: #f92;
                        font-size: 24px;
                    }
                }
            }
        }
        article{
            @include list(row);
            align-items: center;
            padding-left: 30px;
            .wrapper{
                width: 144px;
                height: 10px;
                background: #f3f5f7;
                border-radius: 10px;
                .inner{
                    max-width: 100%;
                    height: 10px;
                    background-image: linear-gradient(270deg,#f55 1%,#ff9c31);
                    border-radius: 10px;
                }
            }
            p{
                font-size: 24px;
                color: #999;
                height: 24px;
                line-height: 24px;
                text-align: center;
                margin-left: 6px;
            }
        }
    }    
}
</style>
