<template>
  <div id="app">
    <Header></Header>
    <router-view />
    <Footer></Footer>
    <div class="msg-whatsapp">
      <a href="https://wa.me/905549753777" target="_blank"><img src="../src/assets/whatsapp_icon.svg" width="48"
          height="48" alt=""></a>
    </div>
  </div>
</template>
<script>
import Header from "@/components/Header.vue"
import Footer from "@/components/Footer.vue"
export default {

  components: {
    Header,
    Footer,
  },
};
</script>
<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background-color: #E6EDEF;
}

*:focus {
  outline: none;
}



nav {
  padding: 30px;
}

nav a {
  font-weight: bold;
  color: #2c3e50;
}

nav a.router-link-exact-active {
  color: #42b983;
}

.msg-whatsapp {
  width: 48px;
  height: 48px;
  border-radius: 50px;
  background-color: transparent;
  position: fixed;
  bottom: 30px;
  right: 30px;
}

textarea {
  resize: none;
}
</style>
