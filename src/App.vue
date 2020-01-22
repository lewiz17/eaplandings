<template>
  <v-app>
    <v-content>
      <v-container>
        <HeroSection />
        <VideoSection />
        <SliderSection />
        <TestimonioSection />
        <ContactSection />
      </v-container> 
      <div class="footer-section">
        <img src="./assets/icons/logo-white.png" alt="">
      </div>      
    </v-content>
  </v-app>
</template>
<script>
import HeroSection from './components/HeroSection';
import VideoSection from './components/VideoSection';
import SliderSection from './components/SliderSection';
import TestimonioSection from './components/TestimonioSection';
import ContactSection from './components/ContactSection';

export default {
  name: 'App',

  components: {
    HeroSection,
    VideoSection,
    SliderSection,
    TestimonioSection,
    ContactSection
  },

  data: () => ({
    //
  }),
};
</script>
<style lang="scss">

  @import './assets/styles/slick.css';
  @import 'https://fonts.googleapis.com/css?family=Montserrat:400,500,700&display=swap';
  @import 'https://fonts.googleapis.com/css?family=Open+Sans:300,400,700&display=swap';


  /** General carousel duration scroll transition */
  .v-window-x-transition-enter-active,
  .v-window-x-transition-leave-active{
    transition-duration: 1.5s
  }

  body{

    .v-content{
      background-image: url('./assets/icons/bg-landing-final.png');
      background-position: 0 53px;
      background-repeat: no-repeat;
      background-color: #f8f8f8;

      @media screen and (max-width: 769px) {
        background-color: #fff;
        background-image: url('./assets/icons/bg-landing-tablet.png');
        background-position: center 8.5em;
        
      }
    }
    
  }
  .hideOnTab{
    display: block;
    @media screen and (max-width: 769px) {
      display: none !important;
    }
  }

  .container{
    padding: 70px 12px 125px 12px;

    @media (min-width: 1264px){
      max-width: 90%;
    }
    @media (min-width: 1904px){
      max-width: 81%;
    }
    @media screen and (max-width: 769px) {
      padding: 40px 12px 148px 12px;
      width: 95%;
      margin: 0px 20px !important;
    }
    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {

      margin: 0px 10px !important;
      padding: 30px 12px 100px 12px;
    }

            

  }

  .footer-section{
    justify-content: center;
    align-items: center;
    display: flex;
    background: #0F4CEE;
    min-height: 255px;

    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {
      min-height: 140px;

      img{
        max-width: 250px;
      }
    }

  }

  /** General landing elements */
  h1,.title-two,.title-three{
    font-family: "Montserrat";
    font-style: normal;
    font-weight: bold;
    color: #0046FE;
  }
  
  h1{
    font-size: 72px;
    line-height: 80px;
  }
  .title-two{
    font-size: 64px;
    line-height: 80px;

    @media screen and (max-width: 769px) {
      font-size: 50px;
      line-height: 60px;
    }

    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {
      font-size: 30px;
      line-height: 40px;
    }
  }
  .title-three{
    font-size: 52px;
    line-height: 63px;
    color: #0F4CEE;

    @media screen and (max-width: 769px) {
      font-size: 50px;
      line-height: 60px;
    }

    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {
      font-size: 28px;
      line-height: 38px;
    }

  }
  p{
    font-family: "Open Sans";
    font-style: normal;
    font-weight: 300;
    font-size: 24px;
    line-height: 36px;
    color: #828282;

    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {
      font-size: 20px;
      line-height: 30px;
    }
  }
  .btn-inset{
    width: 299px;
    min-height: 103px;
    line-height: 103px;
    text-decoration: none;
    justify-content: center;
    align-items: center;
    display: flex;
    
    font-family: "Montserrat";
    font-style: normal;
    font-weight: bold;
    font-size: 18px;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: #FFFFFF !important;

    background: #F8F8F8;
    box-shadow: inset 6px 4px 10px rgba(185, 185, 185, 0.6), 
    inset -6px -4px 16px #FFFFFF;
    border-radius: 20px;

    &.full{
      width: 100%;

      i{
        min-width: 92%;
      }
    }

    &.light__red{
      i{
        background: #E91E63;
        box-shadow: -6px -6px 16px #FFFFFF, 
        6px 6px 16px rgba(221, 219, 216, 0.4), 
        4px 4px 50px rgba(233, 30, 99, 0.2);
      }
    }
    &.light__blue{
      i{
        background: #0046FE;
        box-shadow: -6px -6px 16px #FFFFFF, 
        6px 6px 16px rgba(221, 219, 216, 0.4), 
        4px 4px 20px rgba(25, 0, 180, 0.2);
      }
    }
    &.light__purple{
      i{
        background: #C228D6;
        box-shadow: -6px -6px 16px #FFFFFF,
        6px 6px 16px rgba(221, 219, 216, 0.4),
        4px 4px 50px rgba(194, 40, 214, 0.2);
      }
    }
    &.light__green{ 
      i{
        background: #00E4D7;
        box-shadow: -6px -6px 16px #FFFFFF,
        6px 6px 16px rgba(221, 219, 216, 0.4),
        4px 4px 50px rgba(0, 238, 224, 0.2);
      }
    }


    

    i{
      font-style: normal;
      min-width: 266px;
      min-height: 78px;
      line-height: 78px;
      text-align: center;
      background: #ccc;
      border-radius: 20px;
    }

    &:hover{
      opacity: .8;
    }

    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {

      min-height: 95px;
      line-height: 95px;

      i{
        min-height: 65px;
        line-height: 65px;
      }


    }

  }

  .form-wrap{
    justify-content: flex-end;
    display: flex;
    
    .v-input input:invalid, .v-input textarea:invalid{
      box-shadow: -6px -6px 16px #FFFFFF, 
      inset 6px 4px 12px rgba(0, 0, 0, 0.25), 
      inset -6px -4px 12px #FFFFFF;
      border: 1px solid #fff;
    }
  }
  

  /** Forms fixes landing */
  .v-text-field{
    input{
      background: #F8F8F8;
      box-shadow: -6px -6px 16px #FFFFFF, 
      inset 6px 4px 12px rgba(0, 0, 0, 0.25), 
      inset -6px -4px 12px #FFFFFF;
      border-radius: 15px;
      min-height: 81px;
      padding-left: 30px;
     

      &::placeholder{
        color: rgba(97, 97, 97, 0.3) !important;
      }
    }

    .v-input__slot{

      &::before,
      &::after{
        border: 0px !important;
      }
    }

    padding-bottom: 10px;

    @media screen and (max-width: 769px) {

      input{
        padding-left: 55px;
      }

    }
    @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) {
      
      padding-bottom: 0;
      padding-top: 0;

      input{
        padding-left: 30px;
        min-height: 50px;
      }
    }
  }

.v-carousel{
  .v-responsive__content{
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
  }
}



</style>
