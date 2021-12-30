<template>
  <v-container>
    <h3
      class="mt-10 teal--text font-weight-bold text--lighten-1 text-subheader"
    >
      Experiences
    </h3>
    <v-timeline :dense="$vuetify.breakpoint.smAndDown">
      <v-timeline-item
        v-for="(experience, i) in experiences"
        :key="i"
        fill-dot
        icon="mdi-laptop"
        color="teal ligthen-1"
        icon-color="white"
      >
        <span slot="opposite">{{ experience.time }}</span>
        <v-card class="elevation-2" color="teal ligthen-1">
          <v-card-title class="text-h5">
            {{ experience.title }} - {{ experience.place }}
          </v-card-title>
          <v-card-text>
            {{experience.text}}
          </v-card-text>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        title: "Software Developer",
        place: "Freelancer",
        time: "Jan 2021 - Current",
        text: "I am currently a freelance software developer. I usually accept orders to make websites and android applications"
      },
      {
        title: "Intern Web Development",
        place: "PT. Telekomunikasi Indonesia TBK Ridar",
        time: "Feb 2021 - Mar 2021",
        text: "At my internship, I was assigned to create a management information system as well as a geographic information system"
      },
    ],
  }),
};
</script>

<style scoped>
.text-subheader {
  font-family: "Merriweather", serif;
  font-size: 40px;
}
</style>
