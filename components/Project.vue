<template>
  <v-container>
    <v-row class="mt-10" align-content="center">
      <v-col cols="12" md="6" align-self="center">
        <h5 class="text-h5 font-weight-bold">{{ number }}</h5>
        <h4 class="text-h4 font-weight-bold">
          {{ title }}
        </h4>
        <v-img :src="image" width="100%" class="d-block d-md-none my-3 my-md-0"></v-img>
        <p>
          {{ content }}
        </p>
        <p>
          <span class="font-weight-bold">Code Tools</span> :
          <span v-for="(tool, i) in tools" :key="i"
            >{{ tool }}<span v-if="i != tools.length - 1">, </span>
          </span>
        </p>
        <div>
          <v-btn
            rounded
            link
            :href="link"
            color="cyan lighten-1"
            outlined
            target="blank"
            dark
            :disabled="link == ''"
          >
            <v-icon>mdi-eye-outline</v-icon>
            View
          </v-btn>
        </div>
      </v-col>
      <v-col cols="12" md="6" class="d-none d-md-block">
        <v-card elevation="10">
          <v-img :src="image" width="100%"></v-img>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  props: {
    title: String,
    number: String,
    link: String,
    tools: Array,
    content: String,
    image: String,
  },
};
</script>

<style></style>
