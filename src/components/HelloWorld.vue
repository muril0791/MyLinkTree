<template>
  <v-card class="mx-auto">
    <div class="img">
      <v-avatar color="primary" size="200"></v-avatar>
    </div>
    <v-list nav dense class="mx-auto">
      <v-list-item-group v-model="selectedItem" color="gray--light">
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link
          class="button-access"
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list-item-group>
    </v-list>
  </v-card>
</template>
<style scoped></style>
<script>
import "../css/card.css";
export default {
  data: () => ({
    items: [
      { title: "Portifolio", icon: "mdi-email", to: "/" },
      {
        title: "Github",
        icon: "mdi-account-supervisor-circle",
        to: "/",
      },
      { title: "Linkdin", icon: "mdi-clock-start", to: "/" },
      { title: "Sobre", icon: "mdi-email", to: "/" },
      { title: "Contato", icon: "mdi-email", to: "/" },
      { title: "Instagram", icon: "mdi-email", to: "/" },
    ],
  }),
};
</script>
<style scoped>
.img {
  border-radius: 50%;
}
</style>
