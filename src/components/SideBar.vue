<template>
  <v-navigation-drawer
    v-model="drawer"
    app
    color="#342445"
    mini-variant
    mini-variant-width="80"
  >
    <v-avatar class="d-block text-center mx-auto mt-4 my-10" color="" size="40">
      <v-icon color="#524EED" x-large>fab fa-instalod</v-icon>
    </v-avatar>

    <v-list flat class="mt-5">
      <v-list-item-group v-model="selectedItem">
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          active-class="border"
          v-slot="{ active }"
          :ripple="false"
        >
          <v-list-item-icon>
            <v-icon
              v-text="item.icon"
              :color="active ? 'white' : 'grey lighten-1'"
            ></v-icon>
          </v-list-item-icon>
        </v-list-item>
      </v-list-item-group>
    </v-list>
    <div
      style="
        position: absolute;
        bottom: 20px;
        margin-left: auto;
        margin-right: auto;
        left: 0;
        right: 0;
        text-align: center;
      "
    >
      <v-icon class="mb-5" color="grey lighten-1">fas fa-cog</v-icon>

      <br />
      <v-icon color="grey lighten-1">fas fa-sign-out-alt</v-icon>
    </div>
  </v-navigation-drawer>
</template>

<script>
export default {
  data: () => ({
    selectedItem: 0,
    drawer: null,
    items: [
      { icon: "fas fa-bars" },
      { icon: "far fa-compass" },
      { icon: "fas fa-wallet" },
      { icon: "far fa-comment-dots" },
      { icon: "far fa-calendar-alt" },
      { icon: "far fa-file-alt" },
    ],
  }),
};
</script>
<style>
.border {
  margin-left: 12px;
  margin-right: 12px;
  background: #524eed;
  border-radius: 50%;
  text-decoration: none;
}
.v-list-item-group .v-list-item--active {
  color: white !important;
}
</style>
