<script setup lang="ts">
const desserts = ref([
  {
    image:"../public/images/products/1.jpg",
    name: "Frozen Yogurt",
    calories: 159,
  },
  {
    image:"../public/images/products/1.jpg",
    name: "Ice cream sandwich",
    calories: 237,
  },
  {
    image:"../public/images/products/1.jpg",
    name: "Eclair",
    calories: 262,
  },
  {
    image:"../public/images/products/1.jpg",
    name: "Cupcake",
    calories: 305,
  },
]);

</script>

<template>
  <v-card>
    <div class="header-main">
        <h3 class="text-h6 title font-weight-medium py-4 pl-4 text-white">List</h3>
      </div>
    <v-card-text>
      <!-- fixed-header="true" height="400px" -->
      <v-table >
        <thead>
          <tr>
            <th class="text-left">Name</th>
            <th class="text-left">Calories</th>
            <th class="text-left">Text</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="item in desserts" :key="item.name">
            <td>
                <div class="my-image">
              <img src="/images/products/2.jpg" alt="product" />
            </div>
          </td>
              <td>{{ item.name }}</td>
            <td>{{ item.calories }}</td>
          </tr>
        </tbody>
      </v-table>
    </v-card-text>
  </v-card>
</template>

<style lang="scss">
.header-main{
  background-color: #1ca7c4;
}

.my-image{
  width: 100px;

  img{
    width:100%;
  }
}
</style>
