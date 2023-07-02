<template>
  <Container full-height class="mb-4">
    <TwoColumn>
      <template v-slot:left-col>
        <div class="profile-picture">
          <ProfilPicture src="profile.png" alt="profile_picture" />
        </div>
      </template>
      <template v-slot:right-col>
        <Title text="ABOUT ME" align="left" />
        <p class="mb-1">
          Born in France - Hisae's journey started in a tiny village where his
          parents took this long effort of raising a second child, taking a new
          step in the new century, giving birth to a child that will express his
          will to live by trying to share his stories and his art to all he will
          possibly meet, seeking for their smile, giving them the will to pursue
          their dreams.
        </p>
        <p class="mb-1">
          He joined a 2D/3D animation school in 2018 to enhance his artistic
          skills. Develop a new way of observing, taking the time to question
          teachers about their experiences and how he could take advantage of
          their listening. In love with Japanese culture and aesthetic, he
          decided to take a Japanese class to learn the language.
        </p>
        <p class="mb-2">
          In the same sense, one day, he wants to discover what life is like in
          Japan while working there and benefit from a different worldview. All
          this is due to the culture where everything is so different from his
          usual world. Due to high expectations in today's art world, he
          nevertheless continues to learn more every day, in order to realize
          his goals and bring his dreams to life.
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
