<template>
  <section id="services">
    <div class="content-box-md">
      <div class="container">
        <vertical-heading :header="header"/>
        <div class="row">
          <div class="service-boxes">
            <country-card v-for="country in countries" :key="country.cca3" :country="country"/>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// @ is an alias to /src
import CountryCard from "@/components/CountryCard.vue";
import VerticalHeading from "@/components/VerticalHeading.vue";
import CountryService from "@/services/CountryService.js";

export default {
  name: "CountriesList",
  components: {
    CountryCard,
    VerticalHeading,
  },
  data() {
    return {
      header: {
        verticalHeader : 'Where are you ?',
        BeginnnigText : 'Some',
        FormattedText : 'Countries',      
        EndingText : 'for you',
      },
      countries: null
    }
  },
  created () {
    CountryService.getCountries()
    .then(response => {
      this.countries = response.data;
    })
    .catch(error => {
      console.log(error)
    });
  },
};
</script>

<style scoped>
#services:after {
  content: ' ';
  position: absolute;
  z-index: 1;
}
#services {
  position: relative;
}
#services:before {
  border-bottom: 100px solid #f4f4f4;
  border-right: 100vw solid transparent;
  top: -100px;
}
#services:after {
  border-top: 100px solid #f4f4f4;
  border-left: 100vw solid transparent;
  bottom: -100px;
}
.service-boxes {
  display: table;
  padding-top: 50px;
}
.service-boxes [class*='col-'] {
  padding: 0;
}
#services{
    background: #f4f4f4;
}
</style>
