<template>
  <h1 class="bg-purple text-center py-5 BüyükBaşlık">VERSUS</h1>

  <section name="Oyuncunun Htmli" class="mt-16 mx-14">
    <p class="Başlık mb-2">Oyuncu</p>
    <v-progress-linear v-model="oyuncu.can" height="40" color="green"></v-progress-linear>
  </section>

  <section name="Canavarın Htmli" class="mt-16 mx-14">
    <p class="Başlık mb-2">Canavar</p>
    <v-progress-linear v-model="canavar.can" height="40" color="green"></v-progress-linear>
  </section>

  <section name="Tuşlar" class="text-center mt-7 mx-14">
    <v-btn class="bg-purple mt-1" block size="large">Saldır</v-btn>
    <v-btn class="bg-purple mt-1" block size="large">Pot Bas</v-btn>
    <v-btn class="bg-purple mt-1" block size="large">Özel Atak Yap</v-btn>

  </section>
</template>

<script setup>
import {ref} from "vue"
//Canlar belli seviyeye düşünce renk değişsin

var oyuncu = ref({
 can:70,
 saldırıGücü:250,
 kalkan:500
});

var canavar = ref({
  can: 130,
  saldırıGücü:300,
  kalkan:600,
});




</script>

<style scoped>
.BüyükBaşlık {
  font-size: 60px;
  font-weight: 400;
  font-family: Impact, sans-serif;
}

.Başlık {
  font-size: 30px;
  font-weight: bold;
}
</style>
