<script setup lang="ts">
import BigPicture from "../components/layout/BigPicture.vue";
import Container from "../components/layout/Container.vue";
import FullPicture from "../components/layout/FullPicture.vue";
import Gallery from "../components/layout/Gallery.vue";
import Title from "../components/layout/Title.vue";
import TwoColumn from "../components/layout/TwoColumn.vue";

const gallery = [
  "AiHoshino_end.png",
  "AobaranKeiko.png",
  "Carenend.png",
  "kafka_eye.png",
  "HokusaiKatsushika.png",
  "Kokomi.jpg",
  "Koyanmin.png",
  "ruby_eye.png",
  "MarinwallpaperShi.png",
  "MarinwallpaperSu.png",
  "Narmaya_Selfie.png",
  "OberonCrazy.png",
  "Pdp.png",
  "Remillia_Scarlet.png",
  "Scathach.jpg",
  "tlaloc.png",
  "Zagreus&Dusa2.jpg",
  "channels_banner-textless.png",
  "Makima.png",
];
</script>

<template>
  <Container>
  <BigPicture src="full.png" class="mb-8" />
    <TwoColumn>
      <template v-slot:right-col>
        <Title text="ABOUT ME" align="left" />
        <p class="mb-1">
          Based in France, I'm a character artist in constant search of
          improvement. I like to discover new working methods and receive
          constructive criticism to improve my final renders. Art is a field
          that makes sense to me because mastering its essence is nothing short
          of utopian, but that's enough to make me want to take this journey as
          far as I can.
        </p>
        <p class="mb-8">
          My greatest wish would be to be sufficiently aware of my surroundings
          to be able to transcribe them as best I can onto a sheet of paper with
          the sole aid of my head coupled with my hands. I hope to be able to
          pass on as much knowledge as possible to as many people as possible,
          and to help those who would not otherwise dare to embark on this
          adventure to discover this incredible world of art.
        </p>
      </template>
    </TwoColumn>
    <FullPicture src="HokusaiKatsushika.png" class="mb-8" />
    <Title text="THE GALLERY" align="center" />
    <div class="centered mb-8">
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
    <Gallery :images="gallery" />
  </Container>
</template>
