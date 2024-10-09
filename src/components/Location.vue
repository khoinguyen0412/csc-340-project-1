<template>
    <div>
      <h1>Available branches</h1>
      <ul>
        <!-- Loop over the city_list array from the JSON -->
        <li v-for="city in cities" :key="city.id">
          {{ city.name }} - {{ city.country }}
        </li>
      </ul>
    </div>
  </template>
  
  <script>
  // Import cities.json directly from the assets folder
  import citiesData from '@/assets/data/cities.json';
  
  export default {
    data() {
      return {
        cities: citiesData.city_list  // Access the city_list array inside the imported JSON
      };
    }
  };
  </script>
  
  <style scoped>
  ul {
    list-style-type: none;
    padding: 0;
  }
  
  li {
    padding: 10px 0;
    border-bottom: 1px solid #ccc;
  }
  </style>
  