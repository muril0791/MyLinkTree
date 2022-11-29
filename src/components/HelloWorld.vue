<template>
  <v-container>
    <div class="mx-auto card" style="borde: none">
      <div class="img">
        <v-avatar class="avatar" color="primary" size="250">
          <img src="../assets/MyPic.jpeg" />
        </v-avatar>
      </div>
      <div class="infos">
        <h1>Murilo Ferreira</h1>
        <p>Developer Full-Stack</p>
      </div>
      <v-list nav dense class="mx-auto card">
        <v-list-item-group v-model="selectedItem" color="white">
          <v-list-item
            v-for="item in items"
            :key="item.title"
            :href="item.href"
            :class="item.class"
            link
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
    </div>
  </v-container>
</template>
<style scoped></style>
<script>
import "../css/card.css";
export default {
  data: () => ({
    items: [
      {
        title: "Portifolio",
        icon: "mdi-folder-multiple-outline",
        href: "/portifolio",
        class: "port",
      },
      {
        title: "Sobre",
        icon: "mdi-information-variant",
        href: "/about",
        class: "sobre",
      },
      {
        title: "Github",
        icon: "mdi-github",
        href: "https://github.com/muril0791",
        class: "github",
      },
      {
        title: "Linkedin",
        icon: "mdi-linkedin",
        href: "https://www.linkedin.com/in/murilo-ferreira-21557519b/",
        class: "linkedin",
      },

      {
        title: "Whatsapp",
        icon: "mdi-whatsapp",
        href: "https://wa.me/15981040567",
        class: "whatsapp",
      },
      {
        title: "Instagram",
        icon: "mdi-instagram",
        href: "https://www.instagram.com/murilo.ferreira._/",
        class: "instagram",
      },
    ],
  }),
};
</script>
