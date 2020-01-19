<template>
  <v-row class="video-wrap">
    <v-col lg="7" class="video-section">
      <span class="title-two">Build a resume that you can be proud of</span>
      <p>100+ Integrations. Ensure your clients can easily contract, hire and pay you.</p>
    </v-col>
    <v-col lg="5" class="pa-0 vicon-set">
      <img src="@/assets/icons/iconset-video.png" alt="">
    </v-col>
    <v-col lg="12" class="pa-0 player-wrap">
      <div class="hold-video">
        <div class="video__poster" ref="videoPoster">
          <a href="#" @click.prevent="playVideo()"><v-icon>mdi-play-circle</v-icon></a>
        </div>
        <video ref="videoElem" src="@/assets/video/sample.mp4" controls ></video>
      </div>
      <a href="#" class="btn-inset light__purple"><i>Get started</i></a>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: 'VideoSection',
  data: () => ({
    playing: false
  }),

  methods: {
    playVideo() {
      this.$refs.videoPoster.style.display = "none";
      this.$refs.videoElem.play();
    }
  }
};
</script>

<style lang="scss" scoped>
.video-wrap{
  margin-bottom: 70px;
}

.video-section{

  padding-top: 116px;

  p{
    padding-top: 30px;
  }
}

.vicon-set{
  justify-content: center;
  display: flex;
}

.player-wrap{
  justify-content: center;
  align-items: center;
  display: flex;
  flex-wrap: wrap;
}


.hold-video{
  background: #F8F8F8;
  box-shadow: -6px -6px 16px #FFFFFF,
   6px 6px 16px rgba(209, 205, 199, 0.4),
  inset 6px 4px 12px rgba(0, 0, 0, 0.25),
  inset -6px -4px 12px #FFFFFF;
  border-radius: 15px;
  min-height: 1034px;
  padding: 20px;
  position: relative;
  margin: 65px auto;

  .video__poster{
    position: absolute;
    z-index: 2;
    background: url('../assets/icons/poster-video.png') no-repeat;
    background-position: center;
    background-size: cover;
    min-width: calc(100% - 40px);
    min-height: 992px;
    border-radius: 15px;
    justify-content: center;
    align-items: center;
    display: flex;

    a{
      width: 128px;
      height: 128px;
      background: #F8F8F8;
      box-shadow: -6px -6px 16px #D7D7D7,
      6px 6px 16px rgba(209, 205, 199, 0.4);
      border-radius: 100px;
      text-decoration: none;
      text-align: center;
      line-height: 128px;
      

      i{
        font-size: 73px;
        color: #2410A4;
      }
    }
  }
  video{
    max-width: 100%;
    min-height: 992px;
    border-radius: 15px;
    object-fit:cover;
  }
}


</style>
