<template>
  <div class="container-xl contact-view">
    <MailForm />
  </div>
</template>
<script>
import MailForm from "@/components/MailForm.vue";
export default {

  components: {
    MailForm
  },
};
</script>
<style>
.contact-view {
  height: 750px;
}
</style>