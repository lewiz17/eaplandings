<template>
  <v-row class="contact-wrap">
    <v-col lg="12" class="pa-0 contact-section">
      <span class="title-three">Follow Us</span>
      <div class="follow-section">
        <span class="item-follow">
          <a href=""><img src="@/assets/icons/facebook.png" alt=""></a>          
          14,044 Followers
        </span>
        <span class="item-follow">
          <a href=""><img src="@/assets/icons/instagram.png" alt=""></a>
          733 Followers
        </span>
      </div>
      <span class="title-three">Contact Us</span>
      <div class="social-section">
        <a href=""><img src="@/assets/icons/email.png" alt=""></a>
        <a href=""><img src="@/assets/icons/messenger.png" alt=""></a>
        <a href=""><img src="@/assets/icons/skype.png" alt=""></a>
        <a href=""><img src="@/assets/icons/whatsapp.png" alt=""></a>
        <a href=""><img src="@/assets/icons/slack.png" alt=""></a>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'ContactSection',
  data: () => ({
    
  }),
};
</script>

<style lang="scss" scoped>

.contact-section{
  justify-content: center;
  display: flex;
  flex-flow: column;
  align-items: center;


  @media screen and (max-width: 769px) {
    .follow-section{

      margin-bottom: 85px !important;

      .item-follow{
        margin: 0px 2% !important;

      }
    }

    .social-section{
      min-width: 475px !important;

      a{
        width: 72.6px !important;
        height: 72.6px !important;

        img{
          max-width: 32.1px;
        }
      }
    }

  }

  @media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2) {

    .follow-section{
      flex-flow: column;
      align-items: flex-start;
      margin-bottom: 40px !important;

      .item-follow{
        width: 80%;
        margin-bottom: 10px !important;

        a{
          width: 50px !important;
          height: 50px !important;
          line-height: 50px !important;
        }
      }
    }


    .social-section{
      min-width: 90% !important;

      a{
        width: 50.6px !important;
        height: 50.6px !important;

        img{
          max-width: 20.1px;
        }
      }
    }
  }

  .follow-section{
    width: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 40px;
    margin-bottom: 140px;

    .item-follow{
      display: inline-block;
      margin: 0px 75px;
      font-family: "Open Sans";
      font-style: normal;
      font-weight: 300;
      font-size: 25px;
      line-height: 34px;
      color: #898989;

      a{
        width: 67px;
        height: 67px;
        background: #F8F8F8;
        box-shadow: -6px -6px 16px #FFFFFF,
        6px 6px 16px rgba(209, 205, 199, 0.4);
        border-radius: 15px;
        display: inline-block;
        line-height: 70px;
        text-align: center;
        margin-right: 26px;
        text-decoration: none;

        img{
          max-width: 23px;
        }
      }
      
      
    }
  }

  .social-section{

    min-width: 680px;
    justify-content: space-between;
    display: flex;
    align-items: center;
    margin-top: 50px;

    a{
      display: inline-flex;
      width: 104px;
      height: 104px;
      text-align: center;
      background: #F8F8F8;
      box-shadow: -6px -6px 16px #FFFFFF,
       6px 6px 16px rgba(209, 205, 199, 0.4);
      border-radius: 100px;
      vertical-align: top;
      justify-content: center;
      align-items: center;
      text-decoration: none;
    }
  }
}



</style>
