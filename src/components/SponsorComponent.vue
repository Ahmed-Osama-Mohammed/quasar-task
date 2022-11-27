<template>
  <section class="sponsor">
    <h1 class="title">presenting our proud sponsors</h1>
    <h2 class="sub-title">sponsors & partners</h2>
    <p class="sub-sub-title">platinum sponsors</p>
    <div class="sponsor-detail">
      <div class="container">
        <div class="row">
          <div class="col-12 col-md-6 col-lg-3" v-for="sponsor in sponsors" v-bind:key="sponsor" >
            <div class="sponsor-img">
                <img v-bind:src="sponsor.contentImagePath">
                
            </div>
          </div>
       
        </div>
      </div>
    </div>
    <p class="sub-sub-title">gold sponsors</p>
    <div class="sponsor-detail">
      <div class="container">
        <div class="row">
            <div class="col-12 col-md-6 col-lg-3" v-for="sponsor in sponsors" v-bind:key="sponsor" >
            <div class="sponsor-img">
                <img v-bind:src="sponsor.contentImagePath">
                
            </div>
            </div>
        </div>
      </div>
    </div>
    <p class="sub-sub-title">silver sponsors</p>
    <div class="sponsor-detail">
      <div class="container">
        <div class="row">
            <div class="col-12 col-md-6 col-lg-3" v-for="sponsor in sponsors" v-bind:key="sponsor" >
            <div class="sponsor-img">
                <img v-bind:src="sponsor.contentImagePath">
                </div>
            </div>
        </div>
      </div>
    </div>

    <h1 class="title q-mt-xl q-pt-xl">presenting our exhibitors</h1>
    <h2 class="sub-title">exhibitors</h2>
    <div class="sponsor-detail">
      <div class="container">
        <div class="row">
            <div class="col-12 col-md-6 col-lg-3" v-for="exhibitor in exhibitors" v-bind:key="exhibitor" >
            <div class="sponsor-img">
                <img v-bind:src="exhibitor.contentImagePath">
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import axios from "axios";


export default {
  name: "SponsorComponent",
  data(){
    return {
        sponsors:undefined,
        exhibitors:undefined
    }
  },
  mounted() {

   let headerConfig = { Authorization: "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1laWQiOiIxZDAxZTA1My1kOTRlLTRiMGEtYmQ3ZC03ZGE2ZTNlODg0YzEiLCJ1bmlxdWVfbmFtZSI6IkV2ZW50UmVnaXN0cmF0aW9uLUFkbWluIiwiZW1haWwiOiJhZG1pbkBldmVudHJlZy5jb20iLCJvcmdJRCI6ImJmNWUxNTA3LTE5NTQtNDJhMy1hODRhLTkzNTc3MDcyNTRhNyIsIm5iZiI6MTY2OTQ5OTUwNSwiZXhwIjoxNzMyNjU3OTA1LCJpYXQiOjE2Njk0OTk1MDUsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NTAwMCJ9.YrNgRjt9cgGkd0_4q0wd3Id2SCjZ_C222qGkzmp-b-s" } 
     
   let reqOne=axios.get(
        "https://dev-newconnectedmagixadminapi.azurewebsites.net/admin/v1/organization/bf5e1507-1954-42a3-a84a-9357707254a7/application/9e174a3c-3672-4966-9fa7-85ceef84c580/appcontenttype/sponsor/content?PageNumber=1&PageSize=7",
        { headers: headerConfig }
      )
   let reqTwo=axios.get(
        "https://dev-newconnectedmagixadminapi.azurewebsites.net/admin/v1/organization/bf5e1507-1954-42a3-a84a-9357707254a7/application/9e174a3c-3672-4966-9fa7-85ceef84c580/appcontenttype/exhibitor/content?PageNumber=1&PageSize=7",
        { headers: headerConfig }
      )
   
      axios.all([reqOne, reqTwo]).then(axios.spread((...responses) => {
        this.sponsors=responses[0].data.result.items.slice(0,4);
        this.exhibitors=responses[1].data.result.items.slice(0,4);
    
    }))
    
 

    
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="../css/SponsorComponent.css" scoped></style>
