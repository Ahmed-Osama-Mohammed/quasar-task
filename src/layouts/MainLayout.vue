<template>
 <HeaderComponent/>
 <AboutUsComponent/>
 <SpeakersComponent/>
 <SchuduleComponent/>
 <SponsorComponent/>
 <NewsComponents/>
 <FooterComponent/>
</template>

<script>

import HeaderComponent from '../components/HeaderComponent.vue'
import AboutUsComponent from '../components/AboutUsComponent.vue'
import SpeakersComponent from '../components/SpeakersComponent.vue'
import SchuduleComponent from '../components/SchuduleComponent.vue'
import SponsorComponent from '../components/SponsorComponent.vue'
import NewsComponents from '../components/NewsComponents.vue'
import FooterComponent from '../components/FooterComponent.vue'
export default {
    name: 'MainLayout',

  components: {
    HeaderComponent,
    AboutUsComponent,
    SpeakersComponent,
    SchuduleComponent,
    SponsorComponent,
    NewsComponents,
    FooterComponent
  },

  setup () {
    
  }
}
</script>
