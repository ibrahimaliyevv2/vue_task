<script setup lang="ts">
import { onMounted, ref } from "vue";
import GoogleChart from "./Gchart";
const elementVisible = ref(false);

onMounted(() => {
  setTimeout(() => (elementVisible.value = true), 350);
});
</script>

<template>
  <!-- ------------------------------------ -->
  <!-- html -->
  <!-- ------------------------------------ -->

  <v-card>
    <div class="header-main">
          <h3 class="text-h6 title font-weight-medium py-4 pl-4 text-white">Graph Overview</h3>
        </div>
    <v-card-text>
      <div class="d-sm-flex align-center">
        <v-spacer></v-spacer>
        <div class="ml-auto">
          <div class="d-flex align-center">
            <div class="d-flex align-center px-2">
              <span class="text-primary">
                <span class="text-overline">
                  <i class="mdi mdi-brightness-1 mx-1"></i>
                </span>
                <span class="font-weight-regular">Type1</span>
              </span>
            </div>
            <div class="d-flex align-center px-2">
              <span class="text-secondary">
                <span class="text-overline">
                  <i class="mdi mdi-brightness-1 mx-1"></i>
                </span>
                <span class="font-weight-regular">Type2</span>
              </span>
            </div>
          </div>
        </div>
      </div>
      <div class="mt-5" v-if="elementVisible"><GoogleChart /></div>
    </v-card-text>
  </v-card>
</template>

<style lang="scss">
.header-main{
  background-color: #1ca7c4;
}
</style>