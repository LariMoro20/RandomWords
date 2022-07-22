<template>
  <q-page class="q-pa-md column fit container">
    <div class="flex flex-center q-ma-lg">
      <div class="text-center">
        <div class="text-h2 text-center q-mb-lg text-capitalize">
          {{ word }}
        </div>
        <q-btn color="primary" @click="getWord" label="Nova palavra" /><br />
      </div>
    </div>
    <div class="flex flex-center q-ma-lg">
      <p>
        Sejam bem vindos ao RW! Aqui sortearemos para você e seus amigos uma
        palavra que desafiará vocês no jogo que escolherem. <br />
        <b>Dica de jogo:</b>
        Cada jogador na sua vez sorteia uma palavra e, sem que os demais saibam
        qual é, desenha em um papel ou quadro. Os outros jogadores devem
        adivinhar qual é a palavra sorteada sem que o jogador fale ou a escreva.
        Ganha quem fizer mais pontos e atinjir uma determinada pontuação.
      </p>
      <p>
        Esta aplicação irá constantemente atualizar sua lista de palavras, afim
        de melhorar sua experiência.
      </p>
    </div>
  </q-page>
</template>

<script>
import { defineComponent, ref, onMounted } from "vue";

export default defineComponent({
  name: "PageIndex",
  setup() {
    const jsonData = require("../json/words.json");
    const word = ref("");
    onMounted(() => {
      getWord();
    });
    const getWord = () => {
      let allWords = JSON.parse(JSON.stringify(jsonData));
      const random = Math.floor(Math.random() * allWords.length);
      word.value = allWords[random];
    };

    return { jsonData, word, getWord };
  },
});
</script>
