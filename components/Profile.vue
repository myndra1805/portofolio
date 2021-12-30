<template>
  <div class="p-0">
    <v-list disabled>
      <v-list-item-group>
        <v-list-item v-for="(item, i) in items" :key="i">
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
            <v-list-item-subtitle>{{ item.text }}</v-list-item-subtitle>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </div>
</template>

<script>
export default {
  data: () => ({
    items: [
      {
        title: "Name",
        text: "Ari Yuhendra",
      },
      {
        title: "Gender",
        text: "Male",
      },
      {
        title: "Date of Birth",
        text: "May 18, 1999",
      },
      {
        title: "Address",
        text: "Pekanbaru, Riau, Indonesia",
      },
      {
        title: "Email",
        text: "ariyuhendra99@gmail.com",
      },
      {
        title: "Phone",
        text: "+62-898-8047-067",
      },
    ],
  }),
};
</script>

<style></style>
