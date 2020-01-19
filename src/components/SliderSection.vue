<template>
  <v-row class="slider-wrap">
    <v-col lg="9" class="text-section">
      <span class="title-two">20+ Beautiful Themes  to choose from</span>
      <p>Add your data and then applyany theme tj make your resume visually amazing. Ensure that you stand out  and make a great first impression with any hiring manager.</p>
    </v-col>
    <v-col lg="3" class="pa-0 iconset-slider">
      <img src="@/assets/icons/iconset-slider.png" alt="">
    </v-col>
    <v-col lg="12" class="pa-0 slider-section">
      <div class="hold-slider">
        <slick ref="slick" :options="slickOptions">
          <div class="item-resume">
            <img src="@/assets/imgs/slide1.png" alt=""/>
          </div>
          <div class="item-resume">
            <img src="@/assets/imgs/slide2.png" alt=""/>
          </div>
          <div class="item-resume">
            <img src="@/assets/imgs/slide3.png" alt=""/>
          </div>
        </slick>
        <div class="nav-slider">
          <a href="#" @click.prevent="prev"><img src="@/assets/icons/arrow-left.png" alt=""/></a>
          <span class="navDots"></span>
          <a href="#" @click.prevent="next"><img src="@/assets/icons/arrow-next.png" alt=""/></a>
        </div>
        
      </div>
    </v-col>
  </v-row>
</template>

<script>
import Slick from 'vue-slick';

export default {
  name: 'SliderSection',
  components: {
      Slick
  },
  data: () => ({
    slickOptions: {
      dots: true,
      arrows: false,
      adaptiveHeight: false,
      infinite: true,
      variableWidth: true,
      speed: 800,
      slidesToScroll: 1,
      appendDots: '.navDots'
    },
  }),
  methods: {
    next() {
        this.$refs.slick.next();
    },
    prev() {
        this.$refs.slick.prev();
    }
  }
  
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

.slider-section{
  margin-top: 75px;
}

.hold-slider{
  position: relative;

  .nav-slider{
    width: 431px;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    top: 0px;
    left: 45%;

    a{
      width: 79.3px;
      height: 79.3px;
      background: #F8F8F8;
      box-shadow: -6px -6px 16px #FFFFFF, 
      6px 6px 16px rgba(209, 205, 199, 0.4);
      border-radius: 100px;
      display: flex;
      align-items: center;
      justify-content: center;
      
    }
  }
}

</style>
