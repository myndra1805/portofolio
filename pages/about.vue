<template>
  <v-container class="mb-10">
    <v-row align="center">
      <v-col cols="12" sm="5">
        <v-img src="/images/user.png" alt="" aspect-ratio="1"></v-img>
      </v-col>
      <v-col cols="12" sm="7">
        <h3 class="teal--text font-weight-bold text--lighten-1 title-heading">
          About Me
        </h3>
        <hr
          class="teal lighten-1 rounded-pill"
          style="height: 5px; max-width: 100px"
        />
        <p class="text-body-1 mt-5">
          My name is Ari Yuhendra, I'm a Software Developer and currently
          studying Computer Science. I'm from Riau, Indonesia. Well organised
          person, problem solver, independent with high intention to detail. In
          my works I always try to combine aesthetic with functional aspects,
          looking for the right balance to communicate without annoying.
        </p>
        <Profile />
      </v-col>
    </v-row>
    <Education/>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: "About Me",
    };
  },
};
</script>

<style scoped>
.title-heading {
  font-family: "Merriweather", serif;
  font-size: 60px;
}
</style>
