<template>
  <v-card color="#202022" class="rounded-lg" flat>
    <v-row>
      <v-col cols="12" sm="4">
        <v-card color="transparent" class="rounded-lg mx-2" flat>
          <v-btn color="green" small>
            <v-icon color="white">far fa-dollar-sign</v-icon>
          </v-btn>
          <h2 class="white--text">$8.779,58</h2>
          <h6 class="grey--text">Availlable Ballance</h6>
          <v-btn color="#524EED" dark class="withoutupercase mt-2"
            >Link Accounts</v-btn
          >
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card color="#242426" class="rounded-lg mx-2" flat>
          <v-app-bar flat color="rgba(0, 0, 0, 0)">
            <span class="caption grey--text mt-n6">Sales</span>
          </v-app-bar>
          <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n12">
            <h4 class="white--text">96,50%</h4>
            <span class="caption grey--text ml-2"> + 6.7% </span>
          </v-app-bar>

          <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n10">
            <v-progress-linear
              color="orange"
              height="6"
              value="45"
            ></v-progress-linear>
          </v-app-bar>
          <v-card-text class="pt-0 mt-n4">
            <span class="text-caption grey--text font-weight-light"
              >Yearly Goals</span
            >
          </v-card-text>
        </v-card>
      </v-col>
      <v-col cols="12" sm="4">
        <v-card color="#242426" class="rounded-lg mx-2" flat>
          <v-app-bar flat color="rgba(0, 0, 0, 0)">
            <span class="caption grey--text mt-n6">Sales</span>
          </v-app-bar>
          <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n12">
            <h4 class="white--text">96,50%</h4>
            <span class="caption grey--text ml-2"> + 6.7% </span>
          </v-app-bar>

          <v-app-bar flat color="rgba(0, 0, 0, 0)" class="mt-n10">
            <v-progress-linear
              color="orange"
              height="6"
              value="45"
            ></v-progress-linear>
          </v-app-bar>
          <v-card-text class="pt-0 mt-n4">
            <span class="text-caption grey--text font-weight-light"
              >Yearly Goals</span
            >
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
export default {
  data: () => ({}),
};
</script>
<style></style>
