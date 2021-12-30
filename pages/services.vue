<template>
  <v-container class="p-0 mb-10">
    <v-row align-content="center" class="m-0" style="min-height: 100vh">
      <v-col cols="12" md="6">
        <h3 class="title-heading font-weight-bold teal--text text--lighten-1">
          My Service
        </h3>
        <hr
          class="teal lighten-1 rounded-pill"
          style="height: 5px; max-width: 100px"
        />
        <p class="text-body-1 mt-5" style="max-width: 500px">
          The main area of my expertise is web development and mobile
          development. Build beautiful and interactive Web Application with
          HTML, CSS, and Javascript. I also have full stack development
          experience with Express, Laravel, MongoDB and MySQL. As well as in the
          development of mobile applications using flutter
        </p>
        <v-list two-line>
          <v-list-item v-for="(service, i) in services" :key="i">
            <v-list-item-content>
              <v-list-item-title class="text-h5">{{
                service.title
              }}</v-list-item-title>
              <v-progress-linear
                :value="service.value"
                height="10"
                rounded
                color="teal lighten-1"
              ></v-progress-linear>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-col>
      <v-col
        align-self="center"
        cols="12"
        md="6"
      >
        <div>
          <v-container class="container-tag-cloud"></v-container>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
import TagCloud from "TagCloud";
export default {
  head() {
    return {
      title: "Services",
    };
  },
  data: () => ({
    services: [
      {
        title: "Frontend Development",
        value: 90,
      },
      {
        title: "Backend Development",
        value: 85,
      },
      {
        title: "Mobile Development",
        value: 75,
      },
    ],
    skilss: [
      "HTML",
      "CSS",
      "Javascript",
      "PHP",
      "Flutter",
      "Node JS",
      "Express JS",
      "Vue JS",
      "Bootstrap",
      "Vuetify",
      "Laravel",
      "Dart",
      "MySQL",
      "MongoDB",
      "Tailwind CSS",
    ],
    container: ".container-tag-cloud",
    options: {
      radius: 200,
    },
  }),
  mounted() {
    TagCloud(this.container, this.skilss, this.options);
  },
};
</script>

<style>
.title-heading {
  font-family: "Merriweather", serif;
  font-size: 60px;
}
.tagcloud {
  margin: auto;
  width: 100% !important;
}
</style>
