<template>
  <section id="about">
    <div class="content-box-md">
      <div class="container">
        <div class="row">
          <vertical-heading :header="header"/> 
          <div class="col-md-6">       
            <text-side  :text="text"/>
          </div>           
          <image-side :path="path"/>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import VerticalHeading from "@/components/VerticalHeading.vue";
import TextSide from "@/components/TextSide.vue";
import ImageSide from "@/components/ImageSide.vue";

export default {
  name: "AboutView",
  components: {
    VerticalHeading,
    TextSide,
    ImageSide,
  },
  data() {
    return {
      header: {
        verticalHeader: 'Who are we ?',
        BeginnnigText: 'Let us talk',
        FormattedText: 'about',      
        EndingText: 'ourselves',
      },
      text: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Dolorum sunt, nostrum impedit ut nihil neque molestiae consequuntur, expedita voluptate quisquam velit, quo nisi numquam quasi temporibus vero dolorem amet eius. Lorem ipsum dolor sit.',      
      path: 'https://hawkchill.com/wp-content/uploads/2019/11/flagsofworld2-1.jpg',
    }
  },
};
</script>

<style scoped>
#about {
  background: url(../assets/img/bg/pattern.jpg) center no-repeat fixed;
  background-size: cover;
  overflow: visible;
}
#about p{
  margin: 50px 0;
}
#about img {
  width: 400px;
  height: auto;
}
</style>
