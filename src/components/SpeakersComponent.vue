<template>
    <section class="speakers">
        <h1 class="title">Event speakers</h1>
        <h2 class="sub-title">meet our speakers</h2>
        <div class="speakers-team">
            <div class="container-fluid">
                <div class="row">
                    <div class="col-sm-12 col-md-6 col-lg-3  q-mb-xl q-pb-xl " v-for="speaker in speakers" v-bind:key="speaker.name">
                         <TheSpeaker :data="speaker" />
                        </div>
                    </div>
                </div>
            </div>

    </section>
    </template>

<script>
import TheSpeaker from './TheSpeaker.vue'


export default {
  name: 'SpeakersComponent',
  components: {
  TheSpeaker
  },
  data() {
  return {
    speakers: [
        {name:'nancy orbien'      ,img:require('../assets/speaker1.jpg')},
        {name:'francis weber'     ,img:require('../assets/speaker2.jpg')},
        {name:'kyla orbien'       ,img:require('../assets/speaker3.jpg')},
        {name:'adrian dixon'      ,img:require('../assets/speaker4.jpg')},
        {name:'kenneth deons'     ,img:require('../assets/speaker5.jpg')},
        {name:'dale banks'        ,img:require('../assets/speaker6.jpg')},
        {name:'miriam middileton' ,img:require('../assets/speaker7.jpg')},
        {name:'ellen walton'      ,img:require('../assets/speaker8.jpg')}
    ]
  }
}
    
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="../css/SpeakersComponent.css" scoped>

</style>
