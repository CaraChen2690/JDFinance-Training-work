<template lang="html">
   <section :class="$style.mime">
   		<section :class="$style.login">
   			<img src="http://img12.360buyimg.com/jrpmobile/jfs/t2644/238/1420176553/1442/96e2885/573d96deN06201af5.png?width=100&height=100" alt="">
   			<a href="">会员福利 ></a>
   		</section>
   		<img src="https://img12.360buyimg.com/jrpmobile/jfs/t17458/106/2515774543/37592/beef5db/5af952b3N0a4eb5ea.jpg?width=750&height=280" alt="">
   		<ul>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t8971/199/1863233880/2035/56d04776/59cb5fbdNa7c682c3.png?width=70&height=70" alt="">
   				<p>我的资产</p>
   				<a href="">查看全部资产 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t8836/18/2342020923/2120/a9b7a8ff/59cb6124N31cb2889.png?width=70&height=70" alt="">
   				<p>我的优惠券</p>
   				<a href="">查看全部 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t10264/48/2521964269/2177/cb479501/59f945edNc1197b64.png?width=90&height=90" alt="">
   				<p>我的金币</p>
   				<a href="">赚金币兑好物 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t12115/250/469950434/3906/ad97c994/5a0bdf3aN22efb724.png?width=90&height=90" alt="">
   				<p>我的金条</p>
   				<a href="">查看额度 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t9244/132/2364556535/1134/334cd5d9/59cb612dN5b974dc5.png?width=70&height=70" alt="">
   				<p>我的借钱</p>
   				<a href="">查看全部产品 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t9121/110/2300703915/1348/91af205c/59cb613bN1e749e58.png?width=70&height=70" alt="">
   				<p>我的白条</p>
   				<a href="">去提额 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t9649/171/293125950/1453/4cf0cc2/59cb6162N9c71da0f.png?width=70&height=70" alt="">
   				<p>我的众筹</p>
   				<a href="">查看订单/物流 ></a>
   			</li>
   			<li>
   				<img src="https://img12.360buyimg.com/jrpmobile/jfs/t8014/149/2344686222/2102/341ff316/59cb616bN3e1bd87d.png?width=70&height=70" alt="">
   				<p>我的保障</p>
   				<a href="">全方位保障 ></a>
   			</li>
   		</ul>
   		<div>
   			<img src="https://img12.360buyimg.com/jrpmobile/jfs/t10423/230/287832134/1427/af7e4c86/59cb61b2N53280a30.png?width=70&height=70" alt="">
   			<p>实名认证</p>
   			<a href="">去认证 ></a>
   		</div>
   		<div :class="$style.help">
   			<img src="https://img12.360buyimg.com/jrpmobile/jfs/t9832/294/292213011/2420/30888b3d/59cb61c9Nc2bbc057.png?width=70&height=70" alt="">
   			<p>帮助中心</p>
   			<a href="">></a>
   		</div>
   </section>
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
	.mime{
		.login{
			width: 100%;
			height: 140px;
			line-height: 140px;
			padding: 20px 32px;
			box-sizing: border-box;
			vertical-align: middle;
			background-color: #fff;
			margin-bottom: 20px;
			img{
				width: 100px;
				height: 100px;
			}
			a{
				@include btn($size:28px,$color:#999,$bgcolor:#fff)
				height: 60px;
			    line-height: 60px;
			    margin-top: 20px;
			    float: right;
			}
		}
		>img{
			width: 100%;
			margin-bottom: 20px;
		}
		ul li{
			width: 640px;
			height: 112px;
			line-height: 112px;
			padding: 6px 32px;
			box-sizing: border-box;
			background-color: #fff;
			margin-bottom: 2px;
			img{
				width: 48px;
				height: 48px;
				float: left;
				margin: 26px 26px 26px 0;
			}
			p{
				float: left;
				height: 100px;
				line-height: 100px;
				font-size: 32px;

			}
			a{
				@include btn($size:28px,$color:#999,$bgcolor:#fff)
				height: 100px;
			    line-height: 100px;
			    float: right;
			}
		}
		div{
			width: 640px;
			height: 112px;
			line-height: 112px;
			padding: 6px 32px;
			box-sizing: border-box;
			background-color: #fff;
			margin-top: 20px;
			margin-bottom: 20px;
			img{
				width: 48px;
				height: 48px;
				float: left;
				margin: 26px 26px 26px 0;
			}
			p{
				float: left;
				height: 100px;
				line-height: 100px;
				font-size: 32px;

			}
			a{
				@include btn($size:28px,$color:#999,$bgcolor:#fff)
				height: 100px;
			    line-height: 100px;
			    float: right;
			}
		}
		.help{
			margin-bottom: 120px;
		}
	}
</style>