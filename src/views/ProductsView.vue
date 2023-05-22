<template>
    <div class="container-xl my-5 product-view">
        <h4 v-if="GetLangPref === 'tr'" class="mb-5">Ürünlerimiz</h4>
        <h4 v-if="GetLangPref === 'en'" class="mb-5">Our Products</h4>
        <div class="card-container">
            <Card> <template #img> <img src="../assets/Tip1-Usturmaça-askısı-Harken-150.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Usturmaça Askısı</h5>
                    <div>3-13 mm halat çapına uygun</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Fender Hook</h5>
                    <div>Suitable for 3-13 mm rope diameter</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Tip2-Usturmaça-askısı-Harken-280.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Usturmaça Askısı</h5>
                    <div>6-16 mm halat çapına uygun</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Fender Hook</h5>
                    <div>Suitable for 6-16 mm rope diameter</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Tip3-Usturmaça-askısı-Harken-491.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Usturmaça Askısı</h5>
                    <div>6-16 mm halat çapına uygun, krom</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Fender Hook</h5>
                    <div>Suitable for 6-16 mm rope diameter, chrome</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Bot-bağlama-askısı.png" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Bot Bağlama Askısı</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Boat Strap Hook</h5>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Pilot-merdiveni-askısı.png" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Pilot Merdiveni Askısı</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Pilot Ladder Hook</h5>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Cem-kilit-Harken-150.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Cem Kilit</h5>
                    <div>Harken 150 Alüminyum</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Cam Cleat</h5>
                    <div>Harken 150 Aluminium</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Cem-kilit-Harken-280.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Cem Kilit</h5>
                    <div>Harken 280 Alüminyum</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Cam Cleat</h5>
                    <div>Harken 280 Aluminium</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Cem-kilit-Harken-491.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Cem Kilit</h5>
                    <div>Harken 491 Krom</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Cam Cleat</h5>
                    <div>Harken 491 Chrome</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Koç-boynuzu-Krom.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Koç Boynuzu</h5>
                    <div>125 mm, krom</div>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Cleat</h5>
                    <div>125 mm, chrome</div>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/harken237.jpeg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Harken 237 Halka</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Harken 237 Ring</h5>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/krom-halka.jpg" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Krom Halka</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Chrome Ring</h5>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Uzatmalı-ip-yuvası-krom.png" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Uzatmalı İp Yuvası</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Extended Rope Slot</h5>
                </template>
            </Card>
            <Card> <template #img> <img src="../assets/Çengelli-ip-yuvası.png" alt=""></template>
                <template v-if="GetLangPref === 'tr'" #desc>
                    <h5>Çengelli İp Yuvası</h5>
                </template>
                <template v-if="GetLangPref === 'en'" #desc>
                    <h5>Hook Rope Slot</h5>
                </template>
            </Card>
        </div>
    </div>
</template>

<script>
import Card from "@/components/Card.vue"
export default {

    components: {
        Card,
    },
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
.product-view {
    min-height: 750px;
}

.card-container {
    display: flex;
    flex-wrap: wrap;
    gap: 30px;
    justify-content: center;
}
</style>