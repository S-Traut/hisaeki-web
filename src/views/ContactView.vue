<template>
  <Container full-height class="mb-4">
    <TwoColumn>
      <template v-slot:left-col>
        <div class="profile-picture">
          <ProfilPicture src="AobaranKeiko.png" alt="profile_picture" />
        </div>
      </template>
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
        <p class="mb-2">
          My greatest wish would be to acquire sufficient awareness of my surroundings
          to be able to transcribe them as best I can onto a sheet of paper with
          the sole aid of my head coupled with my hands. I hope to be able to
          pass on as much knowledge as possible to as many people as possible,
          and to help those who would not otherwise dare to embark on this
          adventure to discover this incredible world of art.
        </p>
        <a class="btn" href="mailto:ki.hisae@gmail.com">CONTACT ME</a>
      </template>
    </TwoColumn>
  </Container>
</template>

<script setup lang="ts">
import Container from "../components/layout/Container.vue";
import ProfilPicture from "../components/layout/ProfilPicture.vue";
import Title from "../components/layout/Title.vue";
import TwoColumn from "../components/layout/TwoColumn.vue";
</script>

<style scoped>
.profile-picture {
  display: flex;
  justify-content: end;
  align-items: center;
  height: 100%;
  margin-right: 4rem;
}

@media screen and (max-width: 1080px) {
  .profile-picture {
    margin-bottom: 4rem;
    margin-right: 0;
    justify-content: center; 
  }
}

.about-me {
  display: flex;
  flex-direction: column;
  justify-content: center;
}
</style>
