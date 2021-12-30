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
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate iusto nemo, dolorum rerum earum natus deleniti consequuntur asperiores eum quaerat quasi qui ipsam aliquam dolore excepturi obcaecati doloribus fugit debitis.',
        tools: ['React JS', 'Ethereum', 'Material UI'],
        link: '',
        image: "sistem-ketertelusuran-kelapa-sawit.png"
      },
      {
        title: 'Application Android - Smart Parenting',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate iusto nemo, dolorum rerum earum natus deleniti consequuntur asperiores eum quaerat quasi qui ipsam aliquam dolore excepturi obcaecati doloribus fugit debitis.',
        tools: ['Flutter', 'Firebase'],
        link: 'https://play.google.com/store/apps/details?id=com.paud_fkip_unri.smart_parenting',
        image: "smart-parenting.png"
      },
      {
        title: 'Website - Ruang Belajar',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate iusto nemo, dolorum rerum earum natus deleniti consequuntur asperiores eum quaerat quasi qui ipsam aliquam dolore excepturi obcaecati doloribus fugit debitis.',
        tools: ['Laravel', 'MySQL', 'Bootstrap 4'],
        link: 'https://ruang-belajar.com/',
        image: "ruang-belajar.png"
      },
      {
        title: 'Sistem Informasi Manajemen - R1TA',
        content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate iusto nemo, dolorum rerum earum natus deleniti consequuntur asperiores eum quaerat quasi qui ipsam aliquam dolore excepturi obcaecati doloribus fugit debitis.',
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
