<template>
  <v-container>
    <v-row align-content="center" style="min-height: 100vh" class="mb-10">
      <v-col cols="12" sm="6" align-self="center">
        <h3 class="teal--text text--lighten-1 title-heading">Contact Me</h3>
        <hr
          class="teal lighten-1 rounded-pill mb-10"
          style="height: 5px; max-width: 100px"
        />
        <p class="text-body-1 mt-5">
          I’m interested in freelance opportunities – especially ambitious or large projects. However, if you have other request or question, don't hesitate to call me.  I will be happy to help you by email lazlanrafar@gmail.com
        </p>
      </v-col>
      <v-col cols="12" sm="6" align-self="center" class="pt-sm-3 pt-5">
        <v-list>
          <v-list-item-group color="cyan lighten-1">
            <v-list-item
              v-for="(item, i) in items"
              :key="i"
              link
              :href="item.href"
              target="blank"
            >
              <v-list-item-icon>
                <v-icon v-text="item.icon"></v-icon>
              </v-list-item-icon>
              <v-list-item-content>
                <v-list-item-title v-text="item.text"></v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list-item-group>
        </v-list>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  head() {
    return {
      title: "Contact",
    };
  },
  data: () => ({
    items: [
      { text: "+62-898-8047-067", icon: "mdi-whatsapp", href: "" },
      {
        text: "myndra1805",
        icon: "mdi-github",
        href: "https://github.com/myndra1805",
      },
      {
        text: "ariyuhendra99@gmail.com",
        icon: "mdi-gmail",
        href: "mailto:ariyuhendra99@gmail.com?subject=subject&body=body",
      },
      {
        text: "ari_yuhendra",
        icon: "mdi-instagram",
        href: "https://www.instagram.com/ari_yuhendra/",
      },
      {
        text: "Ari Yuhendra",
        icon: "mdi-linkedin",
        href: "https://www.linkedin.com/in/ari-yuhendra-1b16301bb/",
      },
    ],
  }),
  methods: {
    sendEmail() {
      window.open("mailto:ariyuhendra99@gmail.com?subject=subject&body=body");
    },
  },
};
</script>

<style scoped>
.title-heading {
  font-family: "Merriweather", serif;
  font-size: 60px;
}
</style>
