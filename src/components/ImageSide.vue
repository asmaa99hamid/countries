<template>
  <div class="col-md-6 text-center">
    <img :src=path alt="" />
  </div>
</template>

<script>
export default {
  props: {
    path: String,
  },
};
</script>

<style lang="scss" scoped></style>
