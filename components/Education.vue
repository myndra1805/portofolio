<template>
  <v-container>
    <h3
      class="mt-10 teal--text font-weight-bold text--lighten-1 text-subheader"
    >
      Education &<span style="text-indent: 40px; display: block"
        >Certification</span
      >
    </h3>
    <v-timeline align-top :dense="$vuetify.breakpoint.smAndDown">
      <v-timeline-item
        v-for="(item, i) in educations"
        :key="i"
        color="teal lighten-1"
        :icon="item.icon"
        fill-dot
      >
        <v-card color="teal lighten-1">
          <v-card-title class="mb-3">{{ item.title }}</v-card-title>
          <v-card-subtitle class="white black--text pt-3 pb-0">{{
            item.text
          }}</v-card-subtitle>
          <v-card-subtitle class="white black--text pb-3 py-0">{{
            item.time
          }}</v-card-subtitle>
        </v-card>
      </v-timeline-item>
    </v-timeline>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    educations: [
      {
        text: "Computer Science",
        title: "Universitas Riau",
        icon: 'mdi-school',
        time: "2018 - Current",
      },
      {
        text: "Belajar Membuat Aplikasi Flutter Untuk Pemula",
        title: "Dicoding",
        icon: 'mdi-star',
        time: "Jun 2021 - Jun 2024",
      },
      {
        text: "Membangun Progressive Web Apps",
        title: "Dicoding",
        icon: 'mdi-star',
        time: "Agu 2021 - Agu 2024",
      },
      {
        text: "Belajar Fundamental Front-End Web Development",
        title: "Dicoding",
        icon: 'mdi-star',
        time: "Mei 2021 - Mei 2024",
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
