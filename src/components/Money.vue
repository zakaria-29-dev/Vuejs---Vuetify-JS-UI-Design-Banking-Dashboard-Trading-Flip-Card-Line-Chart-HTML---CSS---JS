<template>
  <v-card color="#202022" class="rounded-lg mt-2" flat>
    <v-row>
      <v-col cols="12" sm="8">
        <v-toolbar color="transparent" flat class="mt-n3">
          <v-toolbar-title class="white--text">
            Money Earned From
          </v-toolbar-title>
          <v-spacer></v-spacer>
          <span class="grey--text">1 Year</span>
          <v-icon x-small color="#878A94" class="ml-2"
            >fas fa-chevron-down</v-icon
          >
        </v-toolbar>
        <Scatter
          :chart-options="chartOptions"
          :chart-data="chartData"
          :chart-id="chartId"
          :dataset-id-key="datasetIdKey"
          :plugins="plugins"
          :css-classes="cssClasses"
          :styles="styles"
          :width="width"
          :height="height"
        />
      </v-col>
      <v-col cols="12" sm="4">
        <v-card color="#242426" class="rounded-lg mr-2" flat>
          <v-toolbar color="transparent" flat class="">
            <v-toolbar-title class="white--text mt-n6"
              >Investation</v-toolbar-title
            >
          </v-toolbar>
          <v-list subheader two-line class="mt-n10" color="transparent">
            <v-list-item v-for="file in files" :key="file.title">
              <v-list-item-avatar rounded>
                <v-icon
                  :class="file.color"
                  dark
                  v-text="file.icon"
                  small
                ></v-icon>
              </v-list-item-avatar>
              <v-list-item-content>
                <v-list-item-title
                  v-text="file.title"
                  class="white--text"
                ></v-list-item-title>
                <v-list-item-subtitle
                  v-text="file.subtitle"
                  class="grey--text"
                ></v-list-item-subtitle>
              </v-list-item-content>
              <v-list-item-action>
                <v-btn icon>
                  <v-icon color="grey lighten-1" small
                    >fas fa-chevron-right</v-icon
                  >
                </v-btn>
              </v-list-item-action>
            </v-list-item>
          </v-list>
        </v-card>
      </v-col>
    </v-row>
  </v-card>
</template>

<script>
import { Scatter } from "vue-chartjs/legacy";

import {
  Chart as ChartJS,
  Title,
  Tooltip,
  Legend,
  LineElement,
  LinearScale,
  CategoryScale,
  PointElement,
} from "chart.js";
ChartJS.register(
  Title,
  Tooltip,
  Legend,
  LineElement,
  LinearScale,
  CategoryScale,
  PointElement
);

export default {
  props: {
    chartId: {
      type: String,
      default: "scatter-chart",
    },
    datasetIdKey: {
      type: String,
      default: "label",
    },
    width: {
      type: Number,
      default: 400,
    },
    height: {
      type: Number,
      default: 180,
    },
    cssClasses: {
      default: "",
      type: String,
    },
    styles: {
      type: Object,
      default: () => {},
    },
    plugins: {
      type: Array,
      default: () => [],
    },
  },
  data: () => ({
    chartData: {
      datasets: [
        {
          label: "S41k/ Income",
          fill: false,
          borderColor: "#f87979",
          backgroundColor: "#f87979",
          data: [
            {
              x: -2,
              y: 4,
            },
            {
              x: -1,
              y: 1,
            },
            {
              x: 0,
              y: 0,
            },
            {
              x: 1,
              y: 1,
            },
            {
              x: 2,
              y: 4,
            },
          ],
        },
        {
          label: "Banking",
          fill: false,
          borderColor: "#524EED",
          backgroundColor: "#524EED",
          data: [
            {
              x: -2,
              y: -4,
            },
            {
              x: -1,
              y: -1,
            },
            {
              x: 0,
              y: 1,
            },
            {
              x: 1,
              y: -1,
            },
            {
              x: 2,
              y: -4,
            },
          ],
        },
      ],
    },
    chartOptions: {
      responsive: true,
      maintainAspectRatio: false,
    },

    /* files */
    files: [
      {
        color: "blue",
        icon: "fas fa-dollar-sign",
        subtitle: "Dolars",
        title: "24",
      },
      {
        color: "green",
        icon: "fas fa-pound-sign",
        subtitle: "Pound ",
        title: "24",
      },
      {
        color: "orange",
        icon: "fas fa-euro-sign",
        subtitle: "Euro",
        title: "24",
      },
    ],
  }),
  components: {
    Scatter,
  },
};
</script>
<style></style>
