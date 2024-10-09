<template>
    <div class="menu-container">
      <h1 class="menu-title">Vietfood Menu</h1>
      <div v-for="(item, index) in menuItems" :key="index" class="menu-item">
        <h2>{{ item.name }}</h2>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </template>
  
  <script>
  // Import the JSON file
  import menuData from '@/assets/data/order.json';

  export default {
    name: 'Menu',
    data() {
      return {
        menuItems: menuData.vietfood_menu
      };
    }
  };
  </script>
  
  <style scoped>
  .menu-container {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
  }
  
  .menu-title {
    text-align: center;
    font-size: 2.5em;
    margin-bottom: 40px;
  }
  
  .menu-item {
    border-bottom: 1px solid #ccc;
    padding: 20px 0;
  }
  
  .menu-item h2 {
    font-size: 1.8em;
    margin-bottom: 10px;
  }
  
  .menu-item p {
    font-size: 1.2em;
    color: #666;
  }
  </style>
  