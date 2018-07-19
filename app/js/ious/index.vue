<template lang="html">
    <div>
        <Heador/>
        <Slider/>
        <Icar></Icar>
        <Iservice></Iservice>
        <Activity></Activity>
        <Footor/>
        <Navbar/>
    </div>
</template>

<script>
import Heador from "../public/header.vue"
import Footor from "../public/footer.vue"
import Navbar from "../public/navbar.vue"
import Slider from "./islider.vue"
import Icar from "./icar.vue"
import Iservice from "./iservice.vue"
import Activity from "./activity.vue"

export default {
    components: {
        Heador,
        Slider,
        Icar,
        Iservice,
        Activity,
        Footor,
        Navbar,
    },
}
</script>
