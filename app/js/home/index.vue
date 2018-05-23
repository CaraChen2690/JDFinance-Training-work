<template lang="html">
	<div>
	    <Heador></Heador>
		<Hslider></Hslider>
		<Money></Money>
		<Product></Product>
		<Insurance></Insurance>
		<Car></Car>
		<Footor></Footor>
		<Navbar></Navbar>
	</div>
</template>

<script>
import Heador from "../public/header.vue";
import Hslider from "./hslider.vue";
import Money from "./money.vue";
import Product from "./product.vue";
import Insurance from "./insurance.vue";
import Car from "./car.vue";
import Footor from "../public/footer.vue";
import Navbar from  "../public/navbar.vue";
export default {
	components: {
		Heador,
		Hslider,
		Money,
		Product,
		Insurance,
		Car,
		Footor,
		Navbar,
	},
}
</script>

