<script setup lang="ts">
import { RouterLink } from "vue-router";
import BigPicture from "../components/layout/BigPicture.vue";
import Container from "../components/layout/Container.vue";
import Gallery from "../components/layout/Gallery.vue";
import Title from "../components/layout/Title.vue";
import TwoColumn from "../components/layout/TwoColumn.vue";
import Image from "../components/layout/Image.vue";

const gallery = [
  "24.jpg",
  "25.jpg",
  "1.jpg",
  "2.jpg",
  "15.jpg",
  "3.jpg",
  "4.jpg",
  "5.jpg",
  "6.jpg",
  "7.jpg",
  "8.jpg",
  "9.jpg",
  "10.jpg",
  "11.jpg",
  "12.jpg",
  "13.jpg",
  "14.jpg",
  "16.jpg",
  "17.jpg",
  "18.jpg",
  "19.jpg",
  "20.jpg",
  "21.jpg",
  "22.jpg",
  "23.jpg",
];
</script>

<template>
  <Container>
    <BigPicture src="title.jpg" class="mb-4" />
    <TwoColumn invert full-height class="mb-1">
      <template v-slot:left-col>
        <div class="signature">
          <Image src="sign.png" />
        </div>
      </template>
      <template v-slot:right-col>
        <div class="whoami">
          <Title align="left" text="WHO AM I?" />
          <p class="mb-1">
            I'm a character artist in constant search of improvement. I like to
            discover new working methods and receive constructive criticism to
            improve my final renders. Art is a field that makes sense to me
            because mastering its essence is nothing short of utopian, but
            that's enough to make me want to take this journey as far as I can.
          </p>
          <p class="mb-2">
            My greatest wish would be to acquire sufficient awareness of my
            surroundings to be able to transcribe them as best I can onto a
            sheet of paper with the sole aid of my head coupled with my hands. I
            hope to be able to pass on as much knowledge as possible to as many
            people as possible, and to help those who would not otherwise dare
            to embark on this adventure to discover this incredible world of
            art.
          </p>
        </div>
      </template>
    </TwoColumn>
    <Title text="THE GALLERY" align="center" />
    <div class="centered mb-4">
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
    <Gallery :images="gallery" class="mb-4" />
    <div class="centered mb-4">
      <p class="mb-1">
        “What makes art great is not the fact that you get great at art, it’s
        that you get great at drawing, it’s that it connects you with the world
        around you, it makes up you a professional human, it makes you a
        professional observer of life.”
      </p>
      <p class="mb-2" style="text-align: right">— Adam Duff LUCIDPIXUL</p>
      <RouterLink to="/contact" class="btn">CONTACT</RouterLink>
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
  .signature {
    margin-right: 0;
  }

  .full-picture {
    height: 600px;
  }
}

.signature > img {
  width: 300px;
  height: auto;
}
</style>
