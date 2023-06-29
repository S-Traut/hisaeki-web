<script setup lang="ts">
import { RouterLink } from "vue-router";
import BigPicture from "../components/layout/BigPicture.vue";
import Container from "../components/layout/Container.vue";
import FullPicture from "../components/layout/FullPicture.vue";
import Gallery from "../components/layout/Gallery.vue";
import ProfilPicture from "../components/layout/ProfilPicture.vue";
import Title from "../components/layout/Title.vue";
import TwoColumn from "../components/layout/TwoColumn.vue";
import Image from "../components/layout/Image.vue";

const gallery = [
  "HokusaiKatsushika.png",
  "Kokomi.jpg",
  "kafka_eye.png",
  "Koyanmin.png",
  "ruby_eye.png",
  "MarinwallpaperShi.png",
  "MarinwallpaperSu.png",
  "Narmaya_Selfie.png",
  "AiHoshino_end.png",
  "OberonCrazy.png",
  "Carenend.png",
  "Pdp.png",
  "Remillia_Scarlet.png",
  "Scathach.jpg",
  "tlaloc.png",
  "Zagreus&Dusa2.jpg",
  "Makima.png",
];
</script>

<template>
  <Container>
    <BigPicture src="Carenend.png" class="mb-8" />
    <TwoColumn invert full-height class="mb-4">
      <template v-slot:left-col>
        <div class="signature">
          <Image src="Sign.png" />
        </div>
      </template>
      <template v-slot:right-col>
        <div class="whoami">
          <Title align="left" text="WHO AM I?" />
          <p class="mb-1">
            I'm a character artist in constant search of improvement. I like to
            discover new working methods and receive constructive criticism to
            improve my final renders. Art is a field that makes sense to me
            because mastering its essence is nothing short of utopian, but that's
            enough to make me want to take this journey as far as I can.
          </p>
          <p class="mb-2">
            My greatest wish would be to acquire sufficient awareness of my
            surroundings to be able to transcribe them as best I can onto a sheet
            of paper with the sole aid of my head coupled with my hands. I hope to
            be able to pass on as much knowledge as possible to as many people as
            possible, and to help those who would not otherwise dare to embark on
            this adventure to discover this incredible world of art.
          </p>
        </div>
      </template>
    </TwoColumn>
    <FullPicture src="AiHoshino_end.png" class="mb-16" />
    <Title text="THE GALLERY" align="center" />
    <div class="centered mb-16">
      <p class="mb-1">
        A work of art can take from a few hours to several days to complete.
        Although time flies when you're focused, it's always important to savor
        that same time, which is the very essence of why I continue to hold a
        pencil over a sheet of paper.
      </p>
      <p>
        Appreciating the whole process of creation is what leads to a result
        that sometimes delights us and reminds us why we started doodling when
        we were young children.
      </p>
    </div>
    <Gallery :images="gallery" class="mb-16" />
    <div class="centered mb-16">
      <p class="mb-1">
        “What makes art great is not the fact that you get great at art, it’s
        that you get great at drawing, it’s that it connects you with the world
        around you, it makes up you a professional human, it makes you a
        professional observer of life.”
      </p>
      <p class="mb-2" style="text-align: right">— Adam Duff LUCIDPIXUL</p>
      <RouterLink to="/contact" class="btn" href="mailto:ki.hisae@gmail.com"
        >CONTACT</RouterLink
      >
    </div>
  </Container>
</template>

<style scoped>
.signature {
  display: flex;
  justify-content: end;
  align-items: center;
  height: 100%;
  margin-right: 4rem;
}

.whoami {
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

@media screen and (max-width: 1080px) {
  .whoami {
    margin-bottom: 8rem; 
  }
}

.signature > img {
  width: 300px;
  height: auto;
}
</style>
