<template>
  <div class="row">
    <div class="col-md-12">
      <div class="vertical-heading">
        <h5>{{ header.verticalHeader }}</h5>
        <h2>
          {{ header.BeginnnigText }} <br />
          <strong>{{ header.FormattedText }}</strong> {{ header.EndingText }}
        </h2>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "VerticalHeading",
  props: {
    header: Object
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.vertical-heading h5 {
  color: #55b9a6;
  font-size: 14px;
  text-transform: uppercase;
  word-spacing: 9px;
  display: inline-block;
  -webkit-transform: translate(-50%) rotate(-90deg);
  -ms-transform: translate(-50%) rotate(-90deg);
  transform: translate(-50%) rotate(-90deg);
  position: relative;
  font-weight: 400;
  top: 56px;
  left: 8px;
}
.vertical-heading h2 {
  font-size: 42px;
  margin: 0 0 0 35px;
  line-height: 45px;
  font-weight: 400;
}
.vertical-heading strong {
  color: #55b9a6;
  font-weight: 700 !important;
}

</style>
