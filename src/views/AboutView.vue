<template>
  <div class="about">
    <div class="bgimg-1 bgimg">
      <div v-if="GetLangPref === 'tr'" class="caption">
        <span class="border">HAKKIMIZDA</span>
      </div>
      <div v-if="GetLangPref === 'en'" class="caption">
        <span class="border">ABOUT US</span>
      </div>
    </div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container">
      <div class="aboutus-text">
        AFS YACHT, geçmişi 1995 yılına dayanan, mevcut ünvanıyla 2010 yılında kurulan bir denizcilik, yatçılık ve
        mühendislik şirketidir.
        Mühendislik hizmetleri, çelik, aluminyum ve paslanmaz konstrüksiyon, donatım ürünleri hizmetleri ile sektörde
        yıllarca çalışmalar yaptık. Halihazırda, yatlara özel olarak tasarlanmış usturmaça askıları ve bağlantılı diğer
        aksesuarları üretiyoruz. 30 yıllık mühendislik tecrübemizle, dünya standartlarında üretim yaparak yüzde yüz
        müşteri memnuniyeti, hızlı üretim ve tatmin garantisi sunuyoruz.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container">
      <div class="aboutus-text">
        AFS YACHT is a maritime, yachting and yachting company founded in 2010 with its current title dating back to 1995.
        is an engineering company.
        In the sector with engineering services, steel, aluminum and stainless construction, equipment products services.
        We have worked for years. Currently, there are fender hangers and other attachments specially designed for yachts.
        We produce accessories. With our 30 years of engineering experience, we produce at world standards and
        We offer customer satisfaction, fast production and satisfaction guarantee.
      </div>
    </div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container even">
      <div class="aboutus-text">
        Firmamızın temel amacı, gemi ve yat sahiplerinin ihtiyaçlarını en iyi şekilde karşılayacak ürünler sunmaktır.
        Usturmaça askılarımız, en kaliteli malzemeler kullanılarak üretilmektedir ve üstün dayanıklılığı ve uzun ömrü ile
        öne çıkmaktadır.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container even">
      <div class="aboutus-text">
        The main purpose of our company is to offer products that best meet the needs of ship and yacht owners.
        Our fender hangers are manufactured using the highest quality materials and are characterized by superior
        durability and longevity.
        stands out.
      </div>
    </div>
    <div class="bgimg-2 bgimg"></div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container">
      <div class="aboutus-text">
        Deneyimli ekibimiz sürekli olarak ürünlerimizi geliştirmek için çalışmaktadır. Bu sayede, müşterilerimizin
        ihtiyaçlarını karşılayacak en son teknolojileri kullanarak, yüksek kaliteli ürünler sunmaktayız.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container">
      <div class="aboutus-text">
        Our experienced team is constantly working to improve our products. In this way, our customers
        We offer high quality products by using the latest technologies to meet their needs.
      </div>
    </div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container even">
      <div class="aboutus-text">
        Firmamız, müşteri memnuniyetine büyük önem vermektedir ve her zaman müşteri odaklı bir yaklaşım benimsemektedir.
        Bu nedenle, müşterilerimizin isteklerini en iyi şekilde anlayarak, en uygun çözümleri sunmak için çalışmaktayız.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container even">
      <div class="aboutus-text">
        Our company attaches great importance to customer satisfaction and always adopts a customer-oriented approach.
        For this reason, we are working to provide the most appropriate solutions by understanding the wishes of our
        customers in the best way.
      </div>
    </div>
    <div class="bgimg-3 bgimg"></div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container">
      <div class="aboutus-text">
        Ayrıca, ürünlerimiz geniş kadromuz ve esnek üretim süreci ile üretilmekte; en kısa sürede müşterilerimize teslim
        edilmektedir. Bu da müşterilerimizin ihtiyaçlarını hızlı bir şekilde karşılamamızı sağlamaktadır.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container">
      <div class="aboutus-text">
        In addition, our products are produced with our large staff and flexible production process; delivery to our
        customers as soon as possible
        is being done. This allows us to quickly meet the needs of our customers.
      </div>
    </div>
    <div v-if="GetLangPref === 'tr'" class="aboutus-container even">
      <div class="aboutus-text">
        Firmamızın ürünlerinde yüksek kalite, hızlı üretim ve müşteri memnuniyeti garantisi sunması, sektörde öne
        çıkmasını sağlamaktadır. Bizimle çalışarak, gemi ve yat sahiplerinin ihtiyaçlarını en iyi şekilde karşılayacak
        ürünleri en kaliteli şekilde elde edebilirsiniz.
      </div>
    </div>
    <div v-if="GetLangPref === 'en'" class="aboutus-container even">
      <div class="aboutus-text">
        The fact that our company offers high quality, fast production and customer satisfaction guarantee in its products
        stands out in the sector.
        provides the output. By working with us, we will meet the needs of ship and yacht owners in the best way.
        You can get the best quality products.
      </div>
    </div>
    <div class="bgimg-4 bgimg"></div>

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
<style scoped>
.bgimg {
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: fixed;
  background-position: center;
  position: relative;
  min-height: 500px;
}

.bgimg-1 {
  background-image: url(../assets/jumbotron-bg-1.jpg);
  min-height: 550px;
}

.bgimg-2 {
  background-image: url(../assets/bg-img1.jpg);
}

.bgimg-3 {
  background-image: url(../assets/bg-img2.jpg);
}

.bgimg-4 {
  background-image: url(../assets/bg-img3.jpg);
}

.caption {
  position: absolute;
  left: 0;
  top: 50%;
  width: 100%;
  text-align: center;
  color: #000;
}

.caption span.border {
  background-color: #001f54;
  color: #fff;
  padding: 18px 8px 18px 18px;
  font-size: 25px;
  letter-spacing: 10px;
}

.aboutus-container {
  width: 100%;
  height: auto;
  padding: 50px 0;
  background-color: #001f54;
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  color: #fff;
}

.even {
  background-color: #E6EDEF;
  color: #000;
}

.aboutus-text {
  width: 60%;
  line-height: 30px;
}

.aboutus-text ul>li {
  list-style: circle;
}

@media (max-width: 992px) {
  .aboutus-text {
    width: 90%;
  }

  .bgimg {
    background-attachment: unset;
  }
}
</style>


