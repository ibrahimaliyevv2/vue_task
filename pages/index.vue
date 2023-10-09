<script setup lang="ts">
import Timeline from "../components/dashboard/timeline/Timeline.vue";
import tables from "./tables.vue";
import GraphOverview from "~/components/dashboard/GraphOverview/GraphOverview.vue";
</script>

<template>
  <v-row>
    <v-col cols="12" sm="12" lg="12"><Timeline /></v-col>
    <v-col cols="12" sm="12" lg="12"><GraphOverview /></v-col>
    <v-col cols="12" sm="12" lg="12"><tables fixedHeader="true" heightLength="400px" /></v-col>
  </v-row>
</template>
