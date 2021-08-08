<template>
  <v-container>
    <v-row>
      <v-col class="text-h3">We'll be in touch!</v-col>
    </v-row>
    <v-row>
      <v-col class="text-h5">
        An Agent will contact you at the address provided to collect further
        information.</v-col
      >
    </v-row>
    <v-row>
      <v-col>
        <v-row
          ><v-col
            ><a> Clinical tr<u>ial inf</u>ormation</a></v-col
          ></v-row
        >
        <v-row
          ><v-col
            ><a>Doctor's <a>info pamp</a>hlet</a></v-col
          ></v-row
        >
        <v-row
          ><v-col
            ><a>Legal disclo<u>ser i</u>nformation</a></v-col
          ></v-row
        >
      </v-col>
      <v-col class="d-flex align-center mb-6">
        <v-img max-height="600" max-width="600" src="@/assets/Blank.png"></v-img
      ></v-col>
    </v-row>
  </v-container>
</template>
<script>
export default {
  methods: {
    goToHome() {
      // `this` will refer to the component instance
      this.$router.push({ name: "Home" });
    },
  },
};
</script>
