<template>
<router-link :to="{ name: 'CountryDetails', params: { code : country.cca3 }}">
  <div class="col-md-4 col-sm-6 col-xs-12">
    <div class="service-box text-center">
      <i class="fa fa-laptop i-blue" aria-hidden="true"></i>
      <h3>{{ country.name.common }}</h3>
      <p>{{CapitalRegion}}</p>
    </div>
  </div>
 </router-link> 
</template>

<script>
export default {
  name: "CountryCard",
  props: {
    country: Object
  },
  computed: {
    CapitalRegion() {
      var text = '';
      if (typeof this.country.capital !== 'undefined')
      {
        text = this.country.capital + ' - ';
      }

      text += this.country.region;

      return text;
    }
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.service-box h3{
  color: #55b9a6;
}
.service-box,
.service-box:after,
.service-box:before{
    -webkit-transition: 0.4s;
  -o-transition: 0.4s;
  transition: 0.4s;
}
.service-box{
  -webkit-box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);
}
.service-box{
  position: relative;
}
.service-box {
  min-height: 270px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 0 15px;
  margin: 10px;
  overflow: hidden;
  box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);
}
.service-box:after,
.service-box:before {
  content: '';
  position: absolute;
  width: 0;
  height: 0;
  border-radius: 50%;
  opacity: 0;
}
.service-box:before {
  left: 0;
  bottom: 0;
  margin-left: -100px;
  margin-bottom: -100px;
}
.service-box:after {
  right: 0;
  top: 0;
  margin-right: -100px;
  margin-top: -100px;
}
.service-box:hover:before {
  width: 180px;
  height: 180px;
  opacity: 0.3;
}
.service-box:hover:after {
  width: 220px;
  height: 220px;
  opacity: 0.3;
}
.service-box i {
  font-size: 36px;
}
.service-box .i-blue {
  color: #3498db;
}
.service-box .i-red {
  color: #e74c3c;
}
.service-box .i-pink {
  color: #9b59b6;
}
.service-box .i-brown {
  color: #795548;
}
.service-box .i-green {
  color: #2ecc71;
}
.service-box .i-yellow {
  color: #f39c12;
}
.service-box h3 {
  margin: 10px 0 15px;
  font-size: 24px;
}
.service-box:hover {
  transform: translateY(-12px);
}
.service-box:after,
.service-box:before{
    background: #55b9a6;
}
</style>
