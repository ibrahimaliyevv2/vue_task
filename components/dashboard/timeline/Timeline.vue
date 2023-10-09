<template>
  <v-card>
    <div class="header-main">
        <h3 class="text-h6 title font-weight-medium py-4 pl-4 text-white">Add new</h3>
      </div>
    <v-card-text>
   
      <div class="profiletimeline position-relative mt-7">
        <v-tabs
      color="deep-purple-accent-4"
      align-tabs="center"
      v-model="tab"
    >
      <v-tab :value="1">Video</v-tab>
      <v-tab :value="2">YouTube</v-tab>
    </v-tabs>
    <v-window v-model="tab">
      <v-window-item :value="1" :key="1">
        <v-file-input clearable label="Choose file"></v-file-input>
      </v-window-item>
      <v-window-item :value="2" :key="2">
          <v-text-field  prepend-icon="mdi-youtube" label="YouTube link"></v-text-field>
      </v-window-item>
    </v-window>
    <div class="end">
        <v-btn color="green" prepend-icon="mdi-check-circle">Add</v-btn>
      </div>
      </div>
      
    </v-card-text>
  </v-card>
</template>

<script>
  export default {
    data: () => ({
      tab: null,
    }),
  }
</script>


<style lang="scss">
.header-main{
  background-color: #1ca7c4;
}
.profiletimeline {
  position: relative;
  .sl-item {
    margin-top: 8px;
    margin-bottom: 30px;
    display: flex;
  }
  .sl-left {
    margin-left: -60px;
    z-index: 1;
    margin-right: 15px;
  }

  .flex-specified{
    display: flex;
    gap:5px;
  }

  .end{
    display:flex;
    justify-content: flex-end;
  }
}
</style>
