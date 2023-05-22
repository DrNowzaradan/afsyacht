<template>
  <div class="container-xl mt-5 ">
    <h4 v-if="GetLangPref === 'tr'" class="mb-5">Bize Ulaşın</h4>
    <h4 v-if="GetLangPref === 'en'" class="mb-5">Contact Us</h4>
    <form v-if="GetLangPref === 'tr'" action="mailto:info@afsyacht.com" method="post" enctype="text/plain">
      <div class="mb-3 col-md-4 mx-auto">
        <label for="nametr" class="form-label">İsim</label>
        <input type="text" name="subject" class="form-control focus-ring focus-ring-dark" id="nametr"
          placeholder="İsminiz..">
      </div>
      <div class="mb-3 col-md-4 mx-auto">
        <label for="emailtr" class="form-label">Email</label>
        <input type="text" name="mail" class="form-control focus-ring focus-ring-dark" id="emailtr" placeholder="Email..">
      </div>
      <div class="mb-3 col-md-4 mx-auto">
        <label for="messagetr" class="form-label">Mesaj</label>
        <textarea type="text" name="body" class="form-control focus-ring focus-ring-dark" id="messagetr"
          placeholder="Mesajınız.." rows="5"></textarea>
      </div>
      <div class="mx-auto col-md-4">
        <button type="submit" value="send" class="btn btn-primary col-12">Gönder</button>
      </div>
    </form>
    <form v-if="GetLangPref === 'en'" action="mailto:info@afsyacht.com" method="post" enctype="text/plain">
      <div class="mb-3 col-md-4 mx-auto">
        <label for="nameen" class="form-label">Name</label>
        <input type="text" name="subject" class="form-control focus-ring focus-ring-dark" id="nameen"
          placeholder="Your Name..">
      </div>
      <div class="mb-3 col-md-4 mx-auto">
        <label for="emailen" class="form-label">Email</label>
        <input type="text" name="email" class="form-control focus-ring focus-ring-dark" id="emailen"
          placeholder="Email..">
      </div>
      <div class="mb-3 col-md-4 mx-auto">
        <label for="messageen" class="form-label">Message</label>
        <textarea type="text" name="body" class="form-control focus-ring focus-ring-dark" id="messageen"
          placeholder="Your message.." rows="5"></textarea>
      </div>
      <div class="mx-auto col-md-4 ">
        <button type="submit" value="send" class="btn btn-primary col-12">Send</button>
      </div>
    </form>
    <hr class="col-md-4 mx-auto">
    <div v-if="GetLangPref === 'tr'" class="mb-3">Sosyal medyada bizi takip edin</div>
    <div v-if="GetLangPref === 'en'" class="mb-3">Follow us on social media</div>
    <div class="icon-group mb-5">
      <a href="https://wa.me/905549753777" target="_blank"><img src="../assets/whatsapp_icon.svg" alt=""></a>
      <a href="https://instagram.com/afsyacht_usturmaca_askisi?igshid=YmMyMTA2M2Y=" target="_blank"><img
          src="../assets/instagram_icon.svg" alt=""></a>
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
.form-label {
  float: left;
  font-weight: 600;
}

.form-control:focus {
  border: 1px solid transparent;
}

.icon-group {
  display: flex;
  justify-content: center;
  gap: 30px;
}

.icon-group img {
  cursor: pointer;
}
</style>