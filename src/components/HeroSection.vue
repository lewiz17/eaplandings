<template>
  <v-row class="hero-wrap">
    <v-col lg="12" sm="12" cols="12" class="pa-0 head-bar">
      <a href="#">
        <img src="@/assets/icons/logo.png" alt="">
      </a>
    </v-col>
    <v-col lg="6" sm="12" cols="12" class="pa-0 intro-section">
      <h1>Make Your Online Resume</h1>
      <p>We believe that resume’s can look beautiful, we help freelancers, contractors &amp; jobseekers create stunning online resume’s.</p>
      <a href="#" class="btn-inset light__red hideOnTab"><i>Get started</i></a>
    </v-col>
    <v-col lg="6" sm="12" cols="12" class="pa-0 form-wrap">
      <div class="hold-form">
        <span class="title-form">
          Create new account
        </span>
        <div class="social-wrap">
          <a href=""><img src="@/assets/icons/instagram.png" alt=""></a>
          <a href=""><img src="@/assets/icons/linkedin.png" alt=""></a>
          <a href=""><img src="@/assets/icons/google.png" alt=""></a>
          <a href=""><img src="@/assets/icons/facebook.png" alt=""></a>
          <a href=""><img src="@/assets/icons/github.png" alt=""></a>
        </div>
        <span class="title-inline">
          or Sign Up with Email
        </span>
        <v-form ref="formSignup" v-model="isValid">
          <v-container>
            <v-row>
              <v-col lg="12" sm="12" cols="12">
                <v-text-field
                  placeholder="Email"
                  v-model="formSignup.email"
                  name="email"
                  :rules="formSignup.emailRules"
                  required
                ></v-text-field>
              </v-col>
              <v-col lg="12" sm="12" cols="12">
                <v-text-field
                  placeholder="Password"
                  v-model="formSignup.password"
                  :rules="formSignup.passwordRules"
                  type="password"
                  name="password"
                  required
                ></v-text-field>
              </v-col>
              <v-col lg="12" sm="12" cols="12">
                <a href="#" class="btn-inset light__blue full" @click.prevent="submitForm"><i>Sign up</i></a>
              </v-col>
            </v-row>
          </v-container>
        </v-form>
        <span class="title-inline">Already have account? <a href="#">Login</a></span>
      </div>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'HeroSection',
  data: () => ({
    formSignup: {
      email: null,
      emailRules: [
          v => !!v || 'E-mail is required',
          v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
      ],
      password: null,
      passwordRules: [
        v => !!v || 'Password is required'
      ]
    },
    isValid: false
  }),
  methods: {
    submitForm() {
      this.$refs.formSignup.validate();
      /** Logic signup */           
    }
  }
};
</script>

<style lang="scss" scoped>
.hero-wrap{
  margin-bottom: 128px;

  @media screen and (max-width: 769px) {
    text-align: center;
    margin-bottom: 50px;

    .head-bar{
      margin-bottom: 65px;

      a{
        img{
          min-width: 316.4px;
          max-height: 53px;
        }
      }
    }

    .intro-section{

      h1{
        margin: 0 auto;
        padding-top: 0;
      } 
      p{
        margin-bottom: 0px;
      }

    }

    .form-wrap{
      justify-content: center;
      max-width: 100%;

      .hold-form{
        max-width: 90%;
        width: 100%;
        padding: 40px 0px;

        .v-form{
          width: 90%;
        }

        .social-wrap{
          max-width: 90%;
        }
      }

    }
  }

  @media only screen 
    and (min-device-width: 320px) 
    and (max-device-width: 480px)
    and (-webkit-min-device-pixel-ratio: 2) { 

    .head-bar{
      margin-bottom: 45px;

      a{
        img{
          min-width: 240px;
          max-width: 240px;
        }
      }
    }

    .intro-section{
      h1{
        font-size: 50px;
        line-height: 55px;
      }
      p{
        font-size: 20px;
        line-height: 30px;
        margin: 0px 10px;
      }
    }
    .hold-form{
      .title-form{
        font-size: 25px;
        line-height: 30px;
      }


    }

    .social-wrap{

      width: 80%;

      a{
        min-width: 45px;
        min-height: 45px;
      }
    }

    .v-form{
      .container{
        >.row{
          flex-flow: column;
        }
      }
    }


  }
  @media only screen 
    and (min-device-width: 770px) 
    and (max-device-width: 1024px) 
    and (-webkit-min-device-pixel-ratio: 1) {
      .form-wrap{
        justify-content: center;
        max-width: 100%;
        align-items: center;
        margin-top: 3%;

        .hold-form{
          max-width: 100%;
        }
      }
  }

}

.head-bar{
  margin-bottom: 100px;
}

.intro-section{
  h1{
    padding-top: 90px;
    max-width: 580px;
  }
  p{
    padding: 30px 0px 45px 0px;
  }
}

.hold-form{
  max-width: 488px;
  padding: 40px;
  background: #F8F8F8;
  box-shadow: -6px -6px 16px #FFFFFF, 6px 6px 16px rgba(209, 205, 199, 0.4);
  border-radius: 15px;
  border: 2px solid #fff;
  justify-content: center;
  display: flex;
  flex-flow: column;
  align-items: center;

  .title-form{
    font-family: "Montserrat";
    font-style: normal;
    font-weight: 500;
    font-size: 30px;
    line-height: 37px;
    color: #0046FE;
  }
  .title-inline{
    font-family: "Montserrat";
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;
    color: #575757;

    a{
      font-weight: bold;
      font-size: 18px;
      line-height: 22px;
      color: #0046FE;
      text-decoration: none;

      &:hover{
        text-decoration: underline;
      }
    }
  }

  .container{
    background: none;
    max-width: 100%;
    padding: 0;
  }

  .v-text-field{
   
    font-family: "Montserrat";
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;

  }

  .btn-inset{
    margin-bottom: 30px;
  }

  .col,.col-12{
    padding: 0;
  }
}



.social-wrap{

  justify-content: space-between;
  display: flex;
  width: 100%;
  margin: 40px auto 55px auto;

  a{
    min-width: 56px;
    min-height: 56px;
    text-align: center;
    background: #F8F8F8;
    box-shadow: -6px -6px 16px #FFFFFF, 
    6px 6px 16px rgba(209, 205, 199, 0.4);
    border-radius: 15px;
    align-items: center;
    justify-content: center;
    display: inline-flex;
    vertical-align: top;

    &:hover{
      box-shadow: -6px -6px 16px #FFFFFF,
       6px 6px 16px rgba(209, 205, 199, 0.4),
        inset 6px 4px 12px rgba(0, 0, 0, 0.25),
        inset -6px -4px 12px #FFFFFF;
        border: 1px solid #fff;
    }
  }
}
</style>
