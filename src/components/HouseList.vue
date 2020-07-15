<template>
  <div>
    <HouseCard
      v-for="house in houses"
      @click="displayHouse(house.id)"
      :key="house.id"
      class="house-card"
    />
  </div>
</template>

<script>
export default {
  name: 'HouseList',

  data() {
    return { houses: [] };
  },

  methods: {
    displayHouse(id) {
      this.$router.push({ path: '/houses', params: { id: id } });
    },
  },
};
</script>

<style>
</style>