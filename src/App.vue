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
  @import 'https://fonts.googleapis.com/css?family=Montserrat:400,500,700&display=swap';
  @import 'https://fonts.googleapis.com/css?family=Open+Sans:300,400,700&display=swap';


  body{

    .v-content{
      // background-attachment: fixed;
      background-image: 
          url('./assets/icons/general-shadow.png'),
          url('./assets/icons/bg-icons.png');
      background-position:
          0 150px,
          0 50px;
      background-repeat: no-repeat;
      background-size: cover;
    }
    
  }

  .container{
    padding: 70px 12px;

    @media (min-width: 1264px){
      max-width: 90%;
    }
    @media (min-width: 1904px){
      max-width: 81%;
    }

  }

  .footer-section{
    justify-content: center;
    align-items: center;
    display: flex;
    background: #0F4CEE;
    min-height: 255px;
  }

  /** General landing elements */
  h1,.title-two{
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
  }
  p{
    font-family: "Open Sans";
    font-style: normal;
    font-weight: 300;
    font-size: 24px;
    line-height: 36px;
    color: #828282;
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
  }

  .form-wrap{
    justify-content: flex-end;
    display: flex;
    
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
      border: 1px solid #fff;
     

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
  }

</style>
