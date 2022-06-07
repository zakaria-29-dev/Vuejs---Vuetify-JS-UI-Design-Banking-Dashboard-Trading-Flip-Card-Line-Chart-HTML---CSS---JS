<template>
  <v-app
    id="inspire"
    :style="{ background: $vuetify.theme.themes.dark.background }"
  >
    <SideBar />
    <v-container>
      <Navbar />
      <v-row>
        <v-col cols="12" sm="8">
          <v-row>
            <v-col cols="12" sm="12">
              <Overview />
            </v-col>
            <v-col cols="12" sm="12">
              <Money />
            </v-col>
            <v-col cols="12" sm="12">
              <Payment />
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" sm="4">
          <Card />
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<script>
// @ is an alias to /src
import SideBar from "../components/SideBar";
import Navbar from "../components/Navbar";
import Overview from "../components/Overview";
import Money from "../components/Money";
import Payment from "../components/Payment";
import Card from "../components/Card";
export default {
  data: () => ({}),
  components: {
    SideBar,
    Navbar,
    Overview,
    Money,
    Payment,
    Card,
  },
};
</script>
<style>
.v-btn.withoutupercase {
  text-transform: none !important;
}
.v-btn:not(.v-btn--round).v-size--small {
  min-width: 30px !important;
  padding: 0 5px !important;
}
</style>
