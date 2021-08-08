<template>
  <v-app>
    <v-container>
      <v-row>
        <v-col class="d-flex align-center mb-6"
          ><v-img
            max-height="150"
            max-width="1300"
            src="@/assets/Banner.png"
          ></v-img
        ></v-col>
      </v-row>
      <v-row>
        <v-col class="text-h3"> Get Back to Living</v-col>
      </v-row>
      <v-row>
        <v-col class="text-h5"
          >Cyzplamovir should be available to everyone who needs it. Can't
          afford it? Enroll here to see if we can help</v-col
        >
      </v-row>
      <v-row>
        <v-col>
          <v-row>
            <v-col
              ><v-text-field
                v-model="firstName"
                label="First name"
                outlined
              ></v-text-field
            ></v-col>
            <v-col
              ><v-text-field
                v-model="lastName"
                label="Last name"
                outlined
              ></v-text-field
            ></v-col>
          </v-row>
          <v-row>
            <v-col
              ><v-text-field
                v-model="addressOne"
                label="Address 1"
                outlined
              ></v-text-field
            ></v-col>
          </v-row>
          <v-row>
            <v-col
              ><v-text-field label="Address 2" outlined></v-text-field
            ></v-col>
          </v-row>
          <v-row>
            <v-col
              ><v-text-field v-model="city" label="City" outlined></v-text-field
            ></v-col>
            <v-col
              ><v-select
                v-model="state"
                :items="items"
                label="State"
                outlined
              ></v-select
            ></v-col>
            <v-col
              ><v-text-field
                v-model="zipcode"
                label="Zipcode"
                outlined
              ></v-text-field
            ></v-col>
          </v-row>
          <v-row>
            <v-col>
              <v-text-field
                v-model="email"
                label="Email"
                outlined
              ></v-text-field
            ></v-col>
          </v-row>
        </v-col>
        <v-col class="pl">
          <v-row>
            <v-col>
              <i
                class="fa fa-lock lock-place"
                style="font-size: 48px; color: black"
              ></i
            ></v-col>
            <v-col
              ><v-btn x-large @click="goToResponse" :disabled="checkIfAllEmpty">
                Enroll
              </v-btn></v-col
            >
          </v-row>
          <v-row>
            <v-col class="quastion-place"><p>Question?</p></v-col>
            <v-col><a>Talk with us</a></v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>
<style scoped>
.lock-place {
  float: right;
}
.quastion-place {
  position: relative;
  left: 37%;
}
.pl {
  margin-top: 20%;
}
.add-margin {
  margin-top: 20%;
}
</style>

<script>
// import TheNavbar from './components/TheNavbar';

export default {
  name: "App",

  //   components: {
  //     TheNavbar,
  //   },

  data() {
    return {
      items: [
        "Maharashtra",
        "Uttar Pradesh",
        "Goa",
        "Gujarat",
        "Karnataka",
        "Rajasthan",
      ],
      firstName: "",
      lastName: "",
      addressOne: "",
      city: "",
      state: "",
      zipcode: "",
      email: "",
    };
  },
  computed: {
    checkIfAllEmpty() {
      if (
        this.firstName.length > 0 &&
        this.lastName.length > 0 &&
        this.addressOne.length > 0 &&
        this.city.length > 0 &&
        this.state.length > 0 &&
        this.zipcode.length > 0 &&
        this.email.length > 0
      ) {
        return false;
      } else {
        return true;
      }
    },
  },
  methods: {
    goToResponse() {
      this.$router.push({ name: "About" });
    },
  },
};
</script>
