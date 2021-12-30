<template>
  <v-container fluid>
    <v-list subheader three-line>
      <v-list-item v-for="(experience, i) in experiences" :key="i">
        <v-list-item-content>
          <v-list-item-title>{{experience.title}} <span class="grey--text">- {{experience.place}}</span></v-list-item-title>
          <v-list-item-subtitle>{{experience.time}}</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        title: 'Software Developer',
        place: 'Freelancer',
        time: 'Jan 2021 - Current'
      },
      {
        title: 'Intern Web Development',
        place: 'Telkom',
        time: 'Feb 2021 - Mar 2021'
      },
    ]
  })
};
</script>

<style></style>
