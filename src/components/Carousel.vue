<template>
    <div class="container-fluid p-0 ">
        <div style="background-color: #fff;">
            <div class="container-xl">
                <div class="product-pair py-3 my-5">
                    <div v-if="GetLangPref === 'tr'" class="product-text">30 yıllık mühendislik tecrübemizle, dünya
                        standartlarında üretim yaparak yüzde yüz müşteri memnuniyeti, hızlı
                        üretim ve tatmin garantisi sunuyoruz.</div>
                    <div v-if="GetLangPref === 'en'" class="product-text">With our 30 years of engineering experience, we
                        produce at world standards and
                        We offer customer satisfaction, fast production and satisfaction guarantee.</div>
                    <img src="../assets/transparan-Fender-hook-Cammatic-150.png" alt="">
                </div>
            </div>
        </div>
        <div class="container-xl">
            <div class="product-pair py-3 my-5">
                <img src="../assets/transparan-Cem-kilit-Harken-491.png" alt="">
                <div v-if="GetLangPref === 'tr'" class="product-text">Firmamızın temel amacı, gemi ve yat sahiplerinin
                    ihtiyaçlarını en iyi şekilde karşılayacak ürünler sunmaktır.
                    Usturmaça askılarımız, en kaliteli malzemeler kullanılarak üretilmektedir ve üstün dayanıklılığı veuzun
                    ömrü ile öne çıkmaktadır.</div>
                <div v-if="GetLangPref === 'en'" class="product-text">The main purpose of our company is to offer products
                    that best meet the needs of ship and yacht owners.
                    Our fender hangers are manufactured using the highest quality materials and are characterized by
                    superior durability and longevity. stands out.</div>
            </div>
        </div>

        <div style="background-color: #fff;">
            <div class="container-xl">
                <div class="product-pair py-3 my-5">
                    <div v-if="GetLangPref === 'tr'" class="product-text">Ürünlerimize göz atmak için ürünler sayfamızı
                        ziyaret edin <br><br>
                        <router-link class="btn btn-primary px-4 py-2" to="/products">Ürünler</router-link>
                    </div>
                    <div v-if="GetLangPref === 'en'" class="product-text">Visit our products page to browse our products
                        <br><br>
                        <router-link class="btn btn-primary px-4 py-2" to="/products">Products</router-link>
                    </div>
                    <img src="../assets/transparan-Koç-boynuzu-Krom.png" alt="">
                </div>
            </div>
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
<style scoped>
.product-pair {
    display: flex;
    align-items: center;
    justify-content: space-between;

}

.product-text {
    max-width: 600px;
}

img {
    width: 400px;
    border-radius: 10px;
}

@media (max-width: 768px) {
    .product-pair {
        display: block;
    }

    .product-text {
        text-align: center;
    }
}
</style>