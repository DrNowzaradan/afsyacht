<template>
  <nav class="navbar sticky-top navbar-dark navbar-expand-lg ">

    <div class="container-xl justify-content-between">
      <router-link class="navbar-brand" to="/home"> <img src="../assets/afsyachtlogowhite.svg" alt=""></router-link>
      <button class="navbar-toggler" id="navbarToggler" type="button" data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent" aria-controls="#navbarSupportedContent" aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul v-if="GetLangPref === 'tr'" class="navbar-nav mx-auto mb-2 mb-lg-0">
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/home">ANASAYFA</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/about-us">HAKKIMIZDA</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/products">ÜRÜNLER</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/contact">İLETİŞİM</router-link>
          </li>
          <li class="nav-item dropdown">
            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              DİL <img src="../assets/tr_icon.svg" width="24" height="24" alt="tr">
            </a>
            <ul class="dropdown-menu dropdown-menu-dark">
              <li><a class="dropdown-item" @click="SwitchLang('tr')">TÜRKÇE<img src="../assets/tr_icon.svg"
                    class="float-end" width="24" height="24" alt="tr"></a></li>
              <li><a class="dropdown-item" @click="SwitchLang('en')">ENGLISH<img src="../assets/en_icon.svg"
                    class="float-end" width="24" height="24" alt="en"></a></li>
            </ul>
          </li>
        </ul>
        <ul v-if="GetLangPref === 'en'" class="navbar-nav mx-auto mb-2 mb-lg-0">
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/home">HOME</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/about-us">ABOUT US</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/products">PRODUCTS</router-link>
          </li>
          <li class="nav-item" @click="CloseToggler()">
            <router-link class="nav-link" exact-active-class="active" exact to="/contact">CONTACT</router-link>
          </li>
          <li class="nav-item dropdown">

            <a class="nav-link dropdown-toggle" href="#" role="button" data-bs-toggle="dropdown" aria-expanded="false">
              LANGUAGE
              <img src="../assets/en_icon.svg" width="24" height="24" alt="en">
            </a>

            <ul class="dropdown-menu dropdown-menu-dark">
              <li><a class="dropdown-item" @click="SwitchLang('tr')">TÜRKÇE<img src="../assets/tr_icon.svg"
                    class="float-end" width="24" height="24" alt="tr"></a></li>
              <li><a class="dropdown-item" @click="SwitchLang('en')">ENGLISH<img src="../assets/en_icon.svg"
                    class="float-end" width="24" height="24" alt="en"></a></li>
            </ul>
          </li>
        </ul>
        <div class="icon-group">
          <a href="https://wa.me/905549753777" target="_blank"><img src="../assets/whatsapp_icon.svg" alt=""></a>
          <a href="https://instagram.com/afsyacht_usturmaca_askisi?igshid=YmMyMTA2M2Y=" target="_blank"><img
              src="../assets/instagram_icon.svg" alt=""></a>

        </div>
      </div>
    </div>
  </nav>
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
      document.getElementById('navbarToggler').click();
    },
    CloseToggler() {
      document.getElementById('navbarToggler').click();
    }
  }
};

</script>
<style scoped>
.navbar {
  width: 100%;
  height: 80px;
  background-color: #001f54;
  display: flex;
  justify-content: center;
  align-items: center;
  position: sticky;
  top: 0;
  z-index: 999;
  text-transform: uppercase;
  --bs-navbar-padding-y: 0;
}

.navbar-brand {
  width: 80px;
  height: 80px;
}

.navbar-nav {
  gap: 30px;
}

.navbar-nav .nav-link {
  font-size: 14px;
  color: #fff;
  border: 1px solid transparent;
}

.navbar-nav .nav-link:hover {
  border-bottom-color: #fff;
}

.navbar-nav .nav-link:focus {
  color: #fff;
}

.navbar-nav .nav-link.active {
  color: #fff;
  border-bottom-color: #fff;
}

.icon-group {
  display: flex;
  justify-content: center;
  gap: 30px;
}

.icon-group img {
  width: 20px;
  height: 20px;
  cursor: pointer;
}

.dropdown-item {
  cursor: pointer;
}

@media (max-width: 992px) {
  .container-xl {
    --bs-gutter-x: 0;
  }

  .navbar-brand {
    margin-left: 20px;
  }

  .navbar-toggler {
    margin-right: 20px;
  }

  .navbar-collapse {
    padding-bottom: 10px;
    background-color: #001f54;
  }
}
</style>