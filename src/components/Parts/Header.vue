<template>
  <div class="flex flex-center q-pa-lg">
    <div class="text-center">
      <img src="images/logo/logo.webp" class="random-logo" /><br />
      <p>
        Site gerador de palavras aleatórias, para brincadeiras como adivinhar o
        desenho
      </p>
    </div>
  </div>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "Header",

  components: {},

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
