<template>
  <div class="home">
    <Jumbotron />

    <Carousel />

    <Form />
  </div>
</template>

<script>
// @ is an alias to /src
import Jumbotron from "@/components/Jumbotron.vue";
import Carousel from "@/components/Carousel.vue";
import Form from "@/components/MailForm.vue";

export default {
  name: "HomeView",
  components: {
    Jumbotron,
    Carousel,
    Form
  },
};
</script>
<style></style>