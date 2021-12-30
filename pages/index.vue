<template>
  <div>
    <div class="jumbotron">
      <v-container style="height: 100%">
        <v-row align="center" style="height: 100%">
          <v-col sm="6" cols="12">
            <h3 class="text-h4 teal--text text--lighten-1">Hello</h3>
            <h1 class="text-h2 font-weight-black teal--text text--lighten-1">
              ARI YUHENDRA
            </h1>
            <h3 class="text-h4 teal--text text--lighten-1">
              Software Developer
            </h3>
            <v-btn to="/about" link nuxt color="teal lighten-1" class="mt-5" x-large outlined rounded>About Me</v-btn>
          </v-col>
          <v-col sm="6" cols="12" class="d-none d-sm-block">
            <v-img src="/images/logo.png" width="100%"></v-img>
          </v-col>
        </v-row>
      </v-container>
    </div>
  </div>
</template>

<script>
export default {
  head() {
    return {
      title: 'Home'
    }
  },
};
</script>

<style scoped>
.jumbotron {
  height: 90vh;
}
</style>
