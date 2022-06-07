<template>
  <v-card color="#202022" class="rounded-lg mt-n3 pb-1" flat>
    <v-toolbar flat color="transparent">
      <v-toolbar-title class="white--text mt-n2">Your Cards</v-toolbar-title>
    </v-toolbar>
    <v-card
      color="#242426"
      class="rounded-lg mx-2 pa-1 mt-n3 gradient flip"
      flat
    >
      <v-toolbar flat color="transparent">
        <v-toolbar-title class="grey--text caption">
          Universal Card
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-icon color="grey" class="">fab fa-cc-mastercard</v-icon>
      </v-toolbar>

      <span class="grey--text mt-3 ml-4 caption">Balance </span>

      <h2 class="white--text ml-4">$4.799,85</h2>

      <v-card-text class="pt-0 mt-4">
        <span class="white--text font-weight-light">**** **** **** 6774</span>
      </v-card-text>
    </v-card>
    <v-toolbar flat color="transparent" class="mt-n2">
      <v-toolbar-title class="white--text">Chats</v-toolbar-title>
      <v-chip color="green" text-color="white" class="ml-2">2</v-chip>
    </v-toolbar>

    <v-list class="mt-n6" color="transparent" dense>
      <v-list-item v-for="chat in chats" :key="chat.title">
        <v-list-item-avatar>
          <v-img :src="chat.img" />
        </v-list-item-avatar>
        <v-list-item-content>
          <v-list-item-title
            v-text="chat.title"
            class="white--text"
          ></v-list-item-title>
          <v-list-item-subtitle
            v-text="chat.subtitle"
            class="grey--text"
          ></v-list-item-subtitle>
        </v-list-item-content>
        <v-list-item-action>
          <h5 class="white--text">{{ chat.date }}</h5>
        </v-list-item-action>
      </v-list-item>
    </v-list>
    <v-card
      color="#242426"
      class="rounded-lg mx-2 pa-1 mt-n3 gradient flip"
      flat
    >
      <h2 class="white--text ml-4">Premium Kit</h2>

      <span class="grey--text mt-4 ml-4 caption"
        >Get out about our new Item</span
      ><br />
      <span class="grey--text ml-4 caption">for community </span>

      <v-card-text class="pt-0 mt-5">
        <v-btn color="#524EED" dark class="withoutupercase mt-2"
          >Trial from $199</v-btn
        >
      </v-card-text>
    </v-card>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    chats: [
      {
        img: "https://cdn.vuetifyjs.com/images/lists/2.jpg",
        subtitle: "Allright then, see you later !",
        title: "Esther Howard",
        date: "12/06/03",
      },
      {
        img: "https://cdn.vuetifyjs.com/images/lists/3.jpg",
        subtitle: "Allright then, see you later ! ",
        title: "Floyd Miles",
        date: "12/06/03",
      },
      {
        img: "https://cdn.vuetifyjs.com/images/lists/4.jpg",
        subtitle: "Allright then, see you later ! ",
        title: "Brooklyn Simmons",
        date: "12/06/03",
      },
    ],
  }),
};
</script>
<style>
.gradient {
  background: rgb(63, 94, 251);
  background: radial-gradient(
    circle,
    rgba(63, 94, 251, 1) 0%,
    rgba(52, 36, 69, 1) 100%
  );
}
.flip {
  transform-style: preserve-3d;
  transition: all 0.8s ease;
}

.flip:hover {
  transform: rotateY(180deg);
}
</style>
