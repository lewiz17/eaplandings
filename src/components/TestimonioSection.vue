<template>
  <v-row class="comments-wrap">
    <v-col lg="12" sm="12" class="pa-0 top-title">
      <span class="title-two">Resume's our users have created</span>
    </v-col>
    <v-col lg="5" sm="12" class="pa-0 top-resumes hideOnTab">
      <div class="item-top">
        <span class="profile_picture"></span>
        <div class="top-info">
          <span class="profile_name">Nikolas Gibson</span>
          <span class="profile_job">Ui Designer</span>
          <a href="#" class="link_see">View resume <v-icon>mdi-eye</v-icon></a>
        </div>
      </div>
      <div class="item-top">
        <span class="profile_picture"></span>
        <div class="top-info">
          <span class="profile_name">Nikolas Gibson</span>
          <span class="profile_job">Ui Designer</span>
          <a href="#" class="link_see">View resume <v-icon>mdi-eye</v-icon></a>
        </div>
      </div>
      <div class="item-top">
        <span class="profile_picture"></span>
        <div class="top-info">
          <span class="profile_name">Nikolas Gibson</span>
          <span class="profile_job">Ui Designer</span>
          <a href="#" class="link_see">View resume <v-icon>mdi-eye</v-icon></a>
        </div>
      </div>

      <a href="#" class="btn-inset light__green"><i>Get started</i></a>

    </v-col>
    <v-col lg="7" sm="12" class="pa-0 author-comment">
      <div class="item-top">
        <v-carousel v-model="carouselState" :show-arrows="false" :hide-delimiters="true" height="290">
          <v-carousel-item>
            <span class="profile_picture"></span>
            <div class="top-info">
              <span class="profile_name">Nikolas Gibson</span>
              <span class="profile_job">Ui Designer</span>
              <a href="#" class="link_see" v-show="windowWidth > 769">View resume <v-icon>mdi-eye</v-icon></a>
              
              <p>Design and build your own higt-quality wabsites. Whether you’re 
                promoting your bussines, showcasing your work,opening 
                your store or starting a blog you can do it all with 
                the 123 resume builder.</p>
              <a href="#" class="link_see" v-show="windowWidth <= 769">View resume <v-icon>mdi-eye</v-icon></a>
                        
              
            </div>
          </v-carousel-item>
          <v-carousel-item>
            <span class="profile_picture photo3"></span>
            <div class="top-info">
              <span class="profile_name">Nikolas Gibson</span>
              <span class="profile_job">Ui Designer</span>
              <a href="#" class="link_see" v-show="windowWidth > 769">View resume <v-icon>mdi-eye</v-icon></a>
              <p>Design and build your own higt-quality wabsites. Whether you’re 
                promoting your bussines, showcasing your work,opening 
                your store or starting a blog you can do it all with 
                the 123 resume builder.</p> 
              <a href="#" class="link_see" v-show="windowWidth <= 769">View resume <v-icon>mdi-eye</v-icon></a>        
            </div>
          </v-carousel-item>
          <v-carousel-item>
            <span class="profile_picture"></span>
            <div class="top-info">
              <span class="profile_name">Nikolas Gibson</span>
              <span class="profile_job">Ui Designer</span>
              <a href="#" class="link_see" v-show="windowWidth > 769">View resume <v-icon>mdi-eye</v-icon></a>
              <p>Design and build your own higt-quality wabsites. Whether you’re 
                promoting your bussines, showcasing your work,opening 
                your store or starting a blog you can do it all with 
                the 123 resume builder.</p>
              <a href="#" class="link_see" v-show="windowWidth <= 769">View resume <v-icon>mdi-eye</v-icon></a>          
            </div>
          </v-carousel-item>
        </v-carousel>
        <div class="paginator" v-if="windowWidth <= 769">
          <div class="nav-carousel">
            <a href="#" @click.prevent="carouselState--"><img src="../assets/icons/arrow-left.png" alt=""></a>
            <a href="#" @click.prevent="carouselState++"><img src="../assets/icons/arrow-next.png" alt=""></a>
          </div>
          <a href="#" class="btn-inset light__green"><i>Get started</i></a>
        </div>
        <div class="nav-carousel" v-else>
          <a href="#" class="link_next" @click.prevent="carouselState++">Next comment <span><img src="@/assets/icons/arrow-next.png" alt=""/></span></a>
        </div>
      </div>
        
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'TestimonioSection',
  data: () => ({
    windowWidth: window.innerWidth,
    carouselState: 0
  }),
  methods: {
    handleWindowResize(e) { this.windowWidth = e.currentTarget.innerWidth; },
  },
  beforeDestroy: function () {
    window.removeEventListener('resize', this. handleWindowResize)
  },
  mounted() {
    window.addEventListener('resize', this.handleWindowResize);
  }
};
</script>

<style lang="scss" scoped>

.comments-wrap{
  margin-bottom: 140px;

  @media screen and (max-width: 769px) {

    margin-top: 30px;
    margin-bottom: 50px;

    .top-resumes{
      order: 3;
    }

    .author-comment{

      margin-top: 50px;
      
      .item-top{
        padding: 0px;

        .profile_picture{
          &.photo3{
            background-image: url('../assets/icons/resume-profile3.png');
          }
        }

        .paginator{
          width: 100%;
          justify-content: center;
          align-items: center;
          display: flex;
          flex-flow: column;

          .nav-carousel{
            justify-content: center;
            align-items: center;
            display: flex;
            margin-bottom: 52px;
            margin-top: 50px;

            a{
              width: 49.7px;
              height: 49.7px;
              min-width: auto;
              margin: 0px 10px;
              background: #F8F8F8;
              box-shadow: -6px -6px 16px #FFFFFF,
              6px 6px 16px rgba(209, 205, 199, 0.4);
              border-radius: 100px;
              text-align: center;
              line-height: 60px;

              img{
                max-width: 22px;
              }

            }
          }
        }
        .top-info{
          padding-top: 20px !important;

          .link_see{
            text-align: left;
          }
          p{  
            font-size: 16px;
            line-height: 36px;
          }
        }
            
      }
    }

    .top-title{
      text-align: center;
    }

    


  }

  @media only screen 
  and (min-device-width: 320px) 
  and (max-device-width: 480px)
  and (-webkit-min-device-pixel-ratio: 2) {

      .author-comment{
        
        .item-top{
          padding: 0px;

          .profile_picture{
            min-width: 100px;
            height: 100px;
            background-size: 85px;
          }

          .top-info{

            min-width: 240px;
            max-width: 240px;

            p{
              margin-top: 18px;
              margin-bottom: 0px;
              font-size: 16px;
              line-height: 25px;
            }

            .profile_name{
              font-size: 20px;
              line-height: 25px;
            }
            .profile_job{
              font-size: 16px;
              line-height: 16px;
              padding-top: 10px;
            }

            .link_see{
              font-size: 16px;
              line-height: 16px;
            }
          }

        }
      }
  }

}

.top-resumes{
  margin-top: 90px;  
}
.item-top{
  font-family: "Montserrat";
  font-style: normal;
  display: flex;
  justify-content: space-between;
  align-items: center;
  max-width: 495px;
  padding: 21px 40px;
  box-shadow: -6px -6px 16px #FFFFFF,
    6px 6px 16px rgba(209, 205, 199, 0.4),
  inset 6px 4px 12px rgba(0, 0, 0, 0.25),
  inset -6px -4px 12px #FFFFFF;
  border-radius: 15px;
  margin-bottom: 40px;
  border: 1px solid #fff;
  background: #f8f8f8;


  .profile_picture{
    display: inline-block;
    width: 105px;
    height: 105px;
    background: url('../assets/icons/resume-profile.png') no-repeat;
    background-size: 84px;
    background-position: center;
    background-color: #F8F8F8;
    box-shadow: -6px -6px 16px #FFFFFF,
      6px 6px 16px rgba(209, 205, 199, 0.4),
      inset 6px 4px 12px rgba(0, 0, 0, 0.25),
      inset -6px -4px 12px #FFFFFF;
    border-radius: 100px;
    border: 2px solid #fff;
  }

  .top-info{
    min-width: 280px;
    padding-top: 14px;

    .profile_name{
      display: block;
      font-weight: bold;
      font-size: 24px;
      line-height: 24px;
      letter-spacing: 0.1em;
      color: #2E64F0;
    }
    .profile_job{
      display: block;
      font-weight: normal;
      font-size: 18px;
      line-height: 18px;
      letter-spacing: 0.1em;
      color: #898989;
      padding-top: 15px;
      padding-bottom: 15px;
    }
    .link_see{
      display: block;
      font-weight: normal;
      font-size: 14px;
      line-height: 14px;
      letter-spacing: 0.1em;
      color: #2E64F0;
      text-decoration: none;
      text-align: right;

      i{
        font-size: 22px;
        color: #2E64F0;
      }

      &:hover{
        opacity: .8;
      }

    }
  }

  &:nth-child(3){
    margin-bottom: 70px;
  }    
}


.author-comment{

  justify-content: flex-end;
  align-items: flex-start;
  display: flex;
  margin-top: 90px;


  .item-top{
    box-shadow: none;
    min-width: 100%;
    border: 0;
    padding: 0 2%;
    background: transparent;
    justify-content: flex-start;
    flex-flow: column;
    align-items: flex-start;

    .profile_picture{
      min-width: 156px;
      height: 156px;
      background: url('../assets/icons/resume-profile2.png') no-repeat;
      background-size: 124.8px;
      background-position: center;
    }

    .top-info{
      max-width:73.5%;
      padding-top: 40px;
      
      .profile_name{
        font-size: 36px;
        line-height: 36px;
      }
      .profile_job{
        font-size: 24px;
        line-height: 24px;
        padding-bottom: 0;
      }

      .link_see{
        font-size: 18px;
        line-height: 18px;

        i{
          font-size: 31px;
        }
      }

      p{
        margin-top: 40px;
      }

     
    }
    .nav-carousel{
      display: flex;
      justify-content: flex-end;
      width: 100%;

      a{
        min-width: 100%;
      }
    }
  }
}
 .link_next{
    display: block;
    text-align: right;
    margin-top: 120px;
    font-family: "Montserrat";
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 18px;
    letter-spacing: 0.1em;
    color: #2E64F0;
    text-decoration: none;

    span{
      width: 70px;
      height: 70px;
      line-height: 70px;
      text-align: center;
      background: #F8F8F8;
      box-shadow: -6px -6px 16px #FFFFFF, 
      6px 6px 16px rgba(209, 205, 199, 0.4);
      border-radius: 100px;
      display: inline-block;
      margin-left: 2%;
      
    }
    
    img{
      vertical-align: middle;
      
    }

    &:hover{
      opacity: .8;
    }
}


</style>
