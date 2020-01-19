<template>
  <v-row class="slider-wrap">
    <v-col lg="9" class="text-section">
      <span class="title-two">20+ Beautiful Themes  to choose from</span>
      <p>Add your data and then applyany theme tj make your resume visually amazing. Ensure that you stand out  and make a great first impression with any hiring manager.</p>
    </v-col>
    <v-col lg="3" class="pa-0 iconset-slider">
      <img src="@/assets/icons/iconset-slider.png" alt="">
    </v-col>
    <v-col lg="12" class="pa-0">
      <div class="hold-slider"></div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'SliderSection',
  data: () => ({
    
  }),
};
</script>

<style lang="scss" scoped>

.text-section{
  padding-top: 156px;
  
  .title-two{
    max-width: 760px;
    display: inline-block;
  }
  p{
    padding-top: 30px;
  }
}

.iconset-slider{
  justify-content: flex-end;
  display: flex;

  img{
    margin-right: -83px;
  }
}

</style>
