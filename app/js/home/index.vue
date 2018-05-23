<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Money/>
        <Product/>
        <Life/>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./hslider.vue"
import Money from "./money.vue"
import Product from "./product.vue"
import Life from "./life.vue"
export default {
    components: {
        Heador,
        Slider,
        Money,
        Product,
        Life,
        Footor,
        Navbar,
    },
}
</script>
