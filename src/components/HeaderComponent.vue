<template>
  <section class="welcome-section ">
    <div class="overlay">
      <q-layout view="hHh lpR fFf">
        <header class="q-header q-layout__section--marginal " data-v-5c833af0="">
          <div class="q-toolbar row no-wrap items-center" role="toolbar" data-v-5c833af0="">
            <div class="q-toolbar__title ellipsis col-12 col-lg-3" data-v-5c833af0="">
              <h4 data-v-5c833af0="">Logo Here</h4>
            </div>
            <div
              class="q-tabs row no-wrap items-center q-tabs--not-scrollable q-tabs--horizontal q-tabs__arrows--inside col-12 col-lg-9 link"
              role="tablist" size="24px" data-v-5c833af0="">
              <!---->
              <div
                class="q-tabs__content row no-wrap items-center self-stretch hide-scrollbar relative-position q-tabs__content--align-center">
                <a class="q-tab relative-position self-stretch flex flex-center text-center q-tab--inactive q-focusable q-hoverable cursor-pointer"
                  tabindex="0" role="tab" aria-selected="false" data-v-5c833af0="">
                  <div class="q-focus-helper" tabindex="-1"></div>
                  <div
                    class="q-tab__content self-stretch flex-center relative-position q-anchor--skip non-selectable column">
                    <div class="q-tab__label">Home</div>
                  </div>
                  <div class="q-tab__indicator absolute-bottom"></div>
                </a><a
                  class="q-tab relative-position self-stretch flex flex-center text-center q-tab--inactive q-focusable q-hoverable cursor-pointer"
                  tabindex="0" role="tab" aria-selected="false" @click="scrollMeTo('about')" data-v-5c833af0="">
                  <div class="q-focus-helper" tabindex="-1"></div>
                  <div
                    class="q-tab__content self-stretch flex-center relative-position q-anchor--skip non-selectable column">
                    <div class="q-tab__label">About Us</div>
                  </div>
                  <div class="q-tab__indicator absolute-bottom"></div>
                </a><a
                  class="q-tab relative-position self-stretch flex flex-center text-center q-tab--inactive q-focusable q-hoverable cursor-pointer"
                  tabindex="0" role="tab" aria-selected="false" data-v-5c833af0="">
                  <div class="q-focus-helper" tabindex="-1"></div>
                  <div
                    class="q-tab__content self-stretch flex-center relative-position q-anchor--skip non-selectable column">
                    <div class="q-tab__label">Speakers</div>
                  </div>
                  <div class="q-tab__indicator absolute-bottom"></div>
                </a><a
                  class="q-tab relative-position self-stretch flex flex-center text-center q-tab--inactive q-focusable q-hoverable cursor-pointer"
                  tabindex="0" role="tab" aria-selected="false" data-v-5c833af0="">
                  <div class="q-focus-helper" tabindex="-1"></div>
                  <div
                    class="q-tab__content self-stretch flex-center relative-position q-anchor--skip non-selectable column">
                    <div class="q-tab__label">Schudule</div>
                  </div>
                  <div class="q-tab__indicator absolute-bottom"></div>
                </a><a
                  class="q-tab relative-position self-stretch flex flex-center text-center q-tab--inactive q-focusable q-hoverable cursor-pointer"
                  tabindex="0" role="tab" aria-selected="false"  data-v-5c833af0="">
                  <div class="q-focus-helper" tabindex="-1"></div>
                  <div
                    class="q-tab__content self-stretch flex-center relative-position q-anchor--skip non-selectable column">
                    <div class="q-tab__label">Sponsors</div>
                  </div>
                  <div class="q-tab__indicator absolute-bottom"></div>
                </a><button
                  class="q-btn q-btn-item non-selectable no-outline q-btn--standard q-btn--rectangle bg-amber text-white q-btn--actionable q-focusable q-hoverable glossy"
                  tabindex="0" type="button" data-v-5c833af0=""><span class="q-focus-helper"></span><span
                    class="q-btn__content text-center col items-center q-anchor--skip justify-center row"><span
                      class="block">Regester Now</span></span></button></div><i
                class="q-icon notranslate material-icons q-tabs__arrow q-tabs__arrow--left absolute q-tab__icon"
                aria-hidden="true" role="presentation">chevron_left</i><i
                class="q-icon notranslate material-icons q-tabs__arrow q-tabs__arrow--right absolute q-tab__icon q-tabs__arrow--faded"
                aria-hidden="true" role="presentation">chevron_right</i>
            </div>
          </div>
          <!---->
        </header>

        <q-page-container>
          <router-view />
        </q-page-container>

      </q-layout>

      <div class="weclome-content px-5 mx-5">
        <div class="container-fluid">
          <div class="row">
            <div class="col-12 col-md-7  title-content">
              <h1 class="title">
                Annual Tech Conference 2022
              </h1>

              <p>
                <q-icon name="today" class="white" size="1em" /> 27 June, 8:00AM | 28 June, 9:30PM
              </p>
              <p>
                <q-icon name="fas fa-map-marker-alt " class="q-pr-xs"/>Grand conference hall st 11341 cairo, Egypt
              </p>
            </div>
            <div class="col-12 col-md-5">
              <div class="reg-side">
                <h1 class="reg-title">
                  Annual Tech Conference 2022
                </h1>
                <p class="reg-add">
                  <q-icon name="fas fa-map-marker-alt" /> Grand conference hall st 11341 cairo, Egypt
                </p>
                <div class="row">
                  <div class="col-6 border-end">
                    <h2>Start Time</h2>
                    <p class="reg-p"> 27 June, 8:00AM </p>
                  </div>
                  <div class="col-6">
                    <h2>End Time</h2>
                    <p class="reg-p"> 28 June, 9:30PM </p>
                  </div>
                </div>
                <a class="reg-button" href="#"> Register now</a>

              </div>
            </div>
          </div>
        </div>
      </div>



    </div>
  </section>



</template>

<script>

export default {
  name: 'HeaderComponent',
  props: {
    msg: String
  }
  ,methods: {
  scrollMeTo(refName) {
    var element = this.$refs[refName];
    var top = element.offsetTop;

    window.scrollTo(0, top);
  }
}
}
</script>
<style src="../css/HeaderComponent.css" scoped>

</style>