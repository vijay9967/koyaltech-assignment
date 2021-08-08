<template>
  <v-app>
    <v-container>
      <TheNav />
      <v-container>
        <router-view />
      </v-container>
    </v-container>
  </v-app>
</template>

<script>
import TheNav from "@/components/TheNav";
export default {
  name: "App",
  components: {
    TheNav,
  },

  data: () => ({
    //
  }),
};
</script>
