<template>
  <v-row>
    <v-col cols="12" sm="6">
      <v-toolbar flat color="transparent" class="mt-n5">
        <v-toolbar-title class="white--text">All Payments</v-toolbar-title>
        <v-chip color="green" text-color="white" class="ml-2">2</v-chip>
      </v-toolbar>
      <v-row>
        <v-col cols="12" sm="6">
          <v-card color="#242426" class="rounded-lg mx-2 pa-2 mt-n3" flat>
            <span class="caption grey--text mt-n6">Credit Card</span><br />
            <h6 class="white--text mt-4">Balance</h6>

            <h4 class="white--text">$767.50</h4>

            <v-card-text class="pt-0">
              <v-icon color="grey" class="mr-2">fab fa-cc-mastercard</v-icon>
              <span class="text-caption grey--text font-weight-light"
                >**6774</span
              >
            </v-card-text>
          </v-card>
        </v-col>
        <v-col cols="12" sm="6">
          <v-card color="#242426" class="rounded-lg mx-2 pa-2 mt-n3" flat>
            <span class="caption grey--text mt-n6">Credit Card</span><br />
            <h6 class="white--text mt-4">Balance</h6>

            <h4 class="white--text">$328.85</h4>

            <v-card-text class="pt-0">
              <v-icon color="grey" class="mr-2">fab fa-cc-visa</v-icon>
              <span class="text-caption grey--text font-weight-light"
                >**6774</span
              >
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
    <v-col cols="12" sm="6">
      <v-toolbar flat color="transparent" class="mt-n5">
        <v-toolbar-title class="white--text">All Transactions</v-toolbar-title>
        <v-chip color="green" text-color="white" class="ml-2">12</v-chip>
      </v-toolbar>
      <v-card color="#242426" class="rounded-lg mr-2 mt-n3" flat>
        <h5 class="white--text ml-2">Recent Experiance</h5>
        <v-list class="mt-n2" color="transparent" dense>
          <v-list-item
            v-for="experience in experiences"
            :key="experience.title"
          >
            <v-list-item-avatar>
              <v-img :src="experience.img" />
            </v-list-item-avatar>
            <v-list-item-content>
              <v-list-item-title
                v-text="experience.title"
                class="white--text"
              ></v-list-item-title>
              <v-list-item-subtitle
                v-text="experience.subtitle"
                class="grey--text"
              ></v-list-item-subtitle>
            </v-list-item-content>
            <v-list-item-action>
              <h5 class="white--text">{{ experience.price }}</h5>
            </v-list-item-action>
          </v-list-item>
        </v-list>
      </v-card>
    </v-col>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    experiences: [
      {
        img: "spotify.png",
        subtitle: "Premium 1 Month Service",
        title: "Spotify",
        price: "-$49.59",
      },
      {
        img: "netflix.png",
        subtitle: "Premium 1 Month Service ",
        title: "Netflix",
        price: "-$106.58",
      },
    ],
  }),
};
</script>
<style></style>
