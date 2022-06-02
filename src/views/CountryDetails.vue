<template>
  <section>
    <div id="advice">
      <div class="content-box-md">
        <div id="services-tabs">
          <div class="service-tab">
            <div class="container">
              <div class="row">
                <image-side :path="path"/>
                <div v-if="country" class="col-md-6">
                    <h3>{{country[0].name.common}}</h3>
                    <text-side :text="text"/>         
                    <div>
                      <a class="btn btn-general btn-blue smooth-scroll" href="#" title="Convert currency to USD">Convert currency to USD</a>
                    </div>
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
import TextSide from "@/components/TextSide.vue";
import ImageSide from "@/components/ImageSide.vue";
import CountryService from "@/services/CountryService.js";

export default {
  name: "CountryDetails",
  props: {
      code: {
          type: [String, Number]
      }
  },
  data() {
      return {
          country:{},
          text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit delectus dignissimos ex aut, nihil iure beatae consequuntur fuga distinctio aspernatur odio magni maiores aperiam ut quisquam nesciunt numquam repellendus amet!',
          path: 'https://static9.depositphotos.com/1712663/1198/v/600/depositphotos_11985568-stock-illustration-circle-flags-of-the-world.jpg'
      }
  },
  components: {
    TextSide,
    ImageSide,
  },
    created () {
    CountryService.getCountry(this.code)
    .then(response => {
        this.country = response.data;
        // console.log(response.data)
    })
    .catch(error => {
        console.log(error)
    });
    },
};
</script>

<style scoped>
#advice {
  position: relative;
  overflow-y: visible;
}
#services-tabs ul li a,
#services-tabs ul li.r-tabs-state-active a{
      font-family: 'Gill Sans', sans-serif;
}
#services-tabs ul {
  margin-bottom: 40px;
}
#services-tabs ul li {
  padding: 5px 30px;
}
#services-tabs ul li a {
  font-size: 14px;
  color: #333;
  font-weight: 400;
  letter-spacing: 1px;
  text-transform: uppercase;
}
.service-tab .col-md-6 {
  padding: 0;
}
.service-tab h2 {
  font-size: 48px;
  color: #bbb;
  margin-bottom: 20px;
  font-weight: 400;
}
.service-tab h3,
.service-tab p {
  margin-bottom: 30px;
}
.service-tab h3 {
  font-size: 32px;
}
#advice{
      background: #fff !important;
}
</style>