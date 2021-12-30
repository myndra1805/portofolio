<template>
  <v-app id="inspire">
    <v-navigation-drawer app v-model="drawer" :mini-variant.sync="mini" class="side-nav">
      <div
        class="d-flex flex-column justify-space-between"
        style="height: 100%"
      >
        <div>
          <v-img src="/images/logo.png" width="100%"></v-img>
        </div>
        <v-list>
          <v-list-item
            v-for="item in links"
            :key="item.title"
            link
            :to="item.href"
            active-class="teal white--text darken-2"
          >
            <v-list-item-icon>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-icon>
          </v-list-item>
        </v-list>
      </div>
    </v-navigation-drawer>
    <v-main>
      <Nuxt />
    </v-main>
    <v-bottom-navigation class="menu-bottombar" fixed style="z-index: 100">
      <v-btn
        color="teal ligthen-1"
        icon
        link
        v-for="item in links"
        :key="item.title"
        :to="item.href"
      >
        <v-icon>{{ item.icon }}</v-icon>
      </v-btn>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    mini: true,
    group: null,
    links: [
      {
        icon: "mdi-home",
        href: "/",
        title: "Home",
      },
      {
        icon: "mdi-account",
        href: "/about",
        title: "About",
      },
      {
        icon: "mdi-tools",
        href: "/services",
        title: "Services",
      },
      {
        icon: "mdi-folder",
        href: "/projects",
        title: "Projects",
      },
      {
        icon: "mdi-phone",
        href: "/contact",
        title: "Contact",
      },
    ],
  }),
};
</script>

<style scoped>
.menu-bottombar {
  display: none;
}
.side-nav {
  display: flex;
}
@media screen and (max-width: 959px) {
  .menu-bottombar {
    display: flex;
  }
  .side-nav {
    display: none;
  }
}
</style>
