
<template>
  <div class="d-flex justify-content-center jumbotron-bg">
    <div v-if="GetLangPref === 'tr'"
      class="container-xl jumbotron-text d-flex flex-column justify-content-start align-items-start">
      <div class="jumbotron-header"> AFSYACHT </div> <br>
      <div class="jumbotron-subtext">AFS YACHT markasıyla 2013 yılından bu yana sizlere hizmet vermekteyiz.</div> <br><br>
      <router-link class="jumbotron-button btn shadow-lg" to="/about-us"> Hakkımızda</router-link>

    </div>
    <div v-if="GetLangPref === 'en'"
      class="container-xl jumbotron-text d-flex flex-column justify-content-start align-items-start">
      <div class="jumbotron-header"> AFSYACHT </div> <br>
      <div class="jumbotron-subtext">We have been serving you since 2013 with the AFS YACHT brand.</div> <br><br>
      <router-link class="jumbotron-button btn shadow-lg" to="/about-us"> About us</router-link>

    </div>
  </div>
</template>
<script>
export default {
  computed: {
    GetLangPref() {
      return this.$store.state.langPref;
    },
  },
  methods: {
    SwitchLang(lang) {
      this.$store.state.langPref = lang
    }
  }
};
</script>
<style>
.jumbotron-bg {
  width: 100%;
  min-height: 880px;
  background-size: cover;
  background-image: linear-gradient(to right, rgba(0, 0, 0, 0.9),
      rgba(0, 0, 0, 0.5)), url(../assets/jumbotron-bg-1.jpg);

}

.jumbotron-header {
  font-size: 52px;
  font-weight: 500;
}

.jumbotron-text {
  position: absolute;
  color: #fff;
  font-size: 22px;
  top: 300px;

}

.jumbotron-subtext {
  max-width: 450px;
  text-align: left;
  color: #f2f2f2;
}

.jumbotron-header,
.jumbotron-subtext {
  font-family: 'Montserrat', sans-serif;
}

.jumbotron-button {
  height: auto;
  font-size: 16px;
  padding: 10px 30px;
  border-radius: 8px;
  border: none;
  outline: none;
  color: #fff;
  background-color: #0077b6;

}

.jumbotron-button:hover {
  background-color: #001f54;
}

@media (max-width: 768px) {
  .jumbotron-bg {
    background-image: linear-gradient(to right, rgba(0, 0, 0, 0.9),
        rgba(0, 0, 0, 0.5)), url(../assets/phone--home-bgimg.jpg);
  }

  .jumbotron-header {
    font-size: 44px;
  }

  .jumbotron-text {
    font-size: 18px;
  }
}
</style>
<!--#001f54-->