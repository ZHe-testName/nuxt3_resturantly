<script setup lang="ts">
import restaurants from "../../data.json";

interface Restaurant {
  id: number;
  rank: number;
  name: string;
  content: string;
  revenue: number;
  numberOfStores: string;
  imageUrl: string; 
};

interface OrganizedInterface {
  first: Restaurant[];
  second: Restaurant[];
};

const restaurantsOrganized: OrganizedInterface = {
  first: [...restaurants].splice(0, 25),
  second: [...restaurants].splice(25, 25),
};
</script>

<template>
  <div class="table">
    <h1>TOP 50: THE RANKING</h1>
    <div class="table-container">
      <div class="table-col">
        <RestaurantRow 
          :is-header="true"
        />
        <RestaurantRow 
          v-for="(res, i) in restaurantsOrganized.first"
          :key="res.id"
          :name="res.name"
          :rank="res.rank"
          :index="i"
        />
      </div>
      <div class="table-col">
        <RestaurantRow 
          :is-header="true"
        />
        <RestaurantRow 
          v-for="(res, i) in restaurantsOrganized.second"
          :key="res.id"
          :name="res.name"
          :rank="res.rank"
          :index="i"
        />
      </div>
    </div>
  </div>
</template>

<style scoped>
.table {
  margin: 3rem 0;
}
.table h1 {
  margin-bottom: 2rem;
}
.table-container {
  display: flex;
  justify-content: space-between;
}
.table-col {
  width: 48%;
}
</style>