<template>
  <div>
    <v-app id="inspire">
      <sidebar></sidebar>
      <v-app-bar color="indigo" dark fixed app>
        <v-app-bar-nav-icon @click.stop="toggleSidebar()"></v-app-bar-nav-icon>
        <v-app-bar-title class="title"><div>Crediti</div></v-app-bar-title>
      </v-app-bar>
      <v-main>Placeholder content</v-main>
    </v-app>
  </div>
</template>
<script>
import sidebar from './Sidebar.vue';

export default {
  components: {
    sidebar
  },
  name: 'Credits',
  methods: {
    toggleSidebar() {
      const currentStatus = this.$store.getters.drawerStatus;
      this.$store.commit('toggleDrawer', !currentStatus);
    },
  },
  data() {
    return {
      drawer: null,
    };
  },
};
</script>
