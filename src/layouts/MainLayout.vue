<template>
  <q-layout class="bg-black">
    <q-page-container class="bg-white">
      <Header />
      <router-view />
      <Footer />
    </q-page-container>
  </q-layout>
</template>

<script>
import Header from "components/Parts/Header.vue";
import Footer from "components/Parts/Footer.vue";
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: { Header, Footer },

  setup() {
    return {};
  },
});
</script>
<style scoped>
.random-logo {
  width: 250px;
}
</style>
