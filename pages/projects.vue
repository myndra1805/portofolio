<template>
  <v-container style="padding: 50px 0">
    <h3
      class="text-center title-heading font-weight-bold teal--text text--lighten-1"
    >
      My Latest Project
    </h3>
    <hr
      class="teal lighten-1 rounded-pill"
      style="height: 5px; max-width: 100px; margin: auto"
    />
    <project v-for="(project, i) in projects" :key="i"
      :title="project.title"
      :content="project.content"
      :image="`/images/projects/${project.image}`"
      :number="`0${i + 1}.`"
      :tools="project.tools"
      :link="project.link"
    ></project>
  </v-container>
</template>

<script>
import Project from '~/components/Project.vue';
export default {
  components: { Project },
  data: () => ({
    projects: [
      {
        title: 'Sistem Ketertelusuran Kelapa Sawit Dengan Blockchain',
        content: 'Sistem ini bertujuan untuk mendeteksi buah kelapa sawit yang masuk ke Pabrik Kelapa Sawit (PKS). PKS cukup memindai QR Code setiap kali ada buah kelapa sawit yang masuk, dan informasi tentang buah kelapa sawit tersebut akan ditampilkan',
        tools: ['React JS', 'Ethereum', 'Material UI'],
        link: '',
        image: "sistem-ketertelusuran-kelapa-sawit.png"
      },
      {
        title: 'Application Android - Smart Parenting',
        content: 'Smart parenting adalah aplikasi yang memuat berbagai informasi mengenai pengasuhan anak usia 0-6 tahun. Aplikasi ini hadir dengan konten mitos fakta, info resiliensi, mediasi digital, bullying, neuro sains dan toilet training. Aplikasi ini bertujuan untuk memberikan pengetahuan kepada orang tua mengenai Pengasuhan pada anak. ',
        tools: ['Flutter', 'Firebase'],
        link: 'https://play.google.com/store/apps/details?id=com.paud_fkip_unri.smart_parenting',
        image: "smart-parenting.png"
      },
      {
        title: 'Website - Ruang Belajar',
        content: 'Ruang Belajar adalah sebuah website untuk siswa kelas 3 SD. Website ini membantu siswa dalam belajar bahasa Indonesia. Didalam website ini terdapat artikel yang dapat dibaca, video yang membantu siswa belajar, dan soal untuk siswa menguji kemampuannya.',
        tools: ['Laravel', 'MySQL', 'Bootstrap 4'],
        link: 'https://ruang-belajar.com/',
        image: "ruang-belajar.png"
      },
      {
        title: 'Sistem Informasi Manajemen - R1TA',
        content: 'Sistem dibuat untuk mengetahui pesebaran ODP, PSB Kendala, dan Sales Activity di Pekanbaru. Pesebarannya akan di tampilkan ke dalam Google Map dan pengguna dapat melihat lokasi masing-masing ODP, PSB Kendala, dan Sales Activity',
        tools: ['Laravel', 'MySQL', 'Vue JS', 'Vuetify'],
        link: 'https://r1ta.com/',
        image: "r1ta.png"
      },
    ]
  }),
  head() {
    return {
      title: "Projects",
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
