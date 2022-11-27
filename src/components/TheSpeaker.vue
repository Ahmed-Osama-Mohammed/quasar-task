<!-- reusable component -->
<template>
                        <img class="speaker-img" v-bind:src="data.img">
                        <h1 class="speaker-name">{{data.name}}</h1>
                        <h1 class="speaker-role">Chairman, EiTESAL</h1>
                        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Tempore voluptatem unde provident. Eos quisquam accusantium, eligendi est ex, repellendus ad neque ea id odio magni obcaecati iusto, harum ipsum ullam.</p>
                        <div class="social">
                            <div class="social-face"><a href="#"><q-icon name="fa-brands fa-facebook" /></a></div>
                            <div class="social-twitter"><a href="#"><q-icon name="fa-brands fa-twitter" /></a></div>
                            <div class="social-linkedin"><a href="#"><q-icon name="fa-brands fa-linkedin-in" /></a></div>
                        </div>
</template>

<script>
export default {
    name:'TheSpeaker',
    props: {
        data : Object
    }
}
</script>
<style src="../css/TheSpeaker.css" scoped>

</style>