<template lang="html">
    <div>
        <Mime></Mime>
        <Navbar/>
    </div>
</template>

<script>
import Mime from "../mime/mime.vue"
import Navbar from "../public/navbar.vue"

export default {
    components: {
        Mime,
        Navbar
    },
}
</script>

<style lang="scss">

</style>
