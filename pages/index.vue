<script setup lang="ts">
import Timeline from "../components/dashboard/timeline/Timeline.vue";
import tables from "./tables.vue";
</script>

<template>
  <v-row>
    <!-- <v-col cols="12" sm="12" lg="8"> <SalesOverview /></v-col> -->
   
    <v-col cols="12" sm="12" lg="12"><Timeline /></v-col>
    <v-col cols="12" sm="12" lg="12"><tables /></v-col>
  </v-row>
</template>
