<template>
    <section class="news">

        <h1 class="title">our event news</h1>
        <h2 class="sub-title">new</h2>
        <div class="news-details">
            <div class="container">
                <div class="row">
                    <div class="col-12 col-md-6" v-for="item in news" v-bind:key="item">
                        <div class="new-card">
                            <div class="row">
                                <div class="col-6">
                                    <h2 class="card-title">{{item.name}}</h2>
                                    <p class="text">{{item.bio}}</p>
                                    <p class="time">{{item.fromtime}}</p>
                                </div>
                                <div class="col-6">
                                    <img v-bind:src="item.contentImagePath">
                                </div>

                            </div>
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
  name: 'NewsComponents',
  data(){
    return {
        news:undefined
    }
  },
  mounted() {
    axios
      .get(
        "https://dev-newconnectedmagixadminapi.azurewebsites.net/admin/v1/organization/bf5e1507-1954-42a3-a84a-9357707254a7/application/9e174a3c-3672-4966-9fa7-85ceef84c580/appcontenttype/news/content?PageNumber=1&PageSize=7",
        { headers: { Authorization: "Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1laWQiOiIxZDAxZTA1My1kOTRlLTRiMGEtYmQ3ZC03ZGE2ZTNlODg0YzEiLCJ1bmlxdWVfbmFtZSI6IkV2ZW50UmVnaXN0cmF0aW9uLUFkbWluIiwiZW1haWwiOiJhZG1pbkBldmVudHJlZy5jb20iLCJvcmdJRCI6ImJmNWUxNTA3LTE5NTQtNDJhMy1hODRhLTkzNTc3MDcyNTRhNyIsIm5iZiI6MTY2OTQ5OTUwNSwiZXhwIjoxNzMyNjU3OTA1LCJpYXQiOjE2Njk0OTk1MDUsImlzcyI6Imh0dHA6Ly9sb2NhbGhvc3Q6NTAwMCJ9.YrNgRjt9cgGkd0_4q0wd3Id2SCjZ_C222qGkzmp-b-s" } }
      )
      .then((res) => {
        this.news = res.data.result.items;
        console.log(this.news);
    });
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style src="../css/NewsComponents.css" scoped>

</style>
