<script>
  export default {
    name: 'ProductSearchList',
    data() {
      return {
        products: [
  {
    id: 1,
    name: "Search Product 1",
    price: 99.99,
    description: "An affordable option for everyday use.",
    usp: "Great for daily tasks.",
    image: "https://placekitten.com/300/200?text=Search+Product+1" 
  },
  {
    id: 2,
    name: "Search Product 2",
    price: 129.99,
    description: "A premium choice for professionals.",
    usp: "High-end features for top-tier performance.",
    image: "https://placekitten.com/300/200?text=Search+Product+2" 
  }
]

      };
    }
  };
  </script>

<template>
    <div class="product-search-list">
      <h2>Product Search List</h2>
      <div v-if="products.length > 0" class="product-cards">
        <div v-for="product in products" :key="product.id" class="product-card">
            <router-link :to="'/product-description/' + product.id">
            <img :src="product.image" alt="Product Image" class="product-image" />
            <h3 class="product-name">{{ product.name }}</h3>
            <p class="product-price">${{ product.price }}</p>
            <p class="product-description">{{ product.description }}</p>
            <p class="product-usp">USP: {{ product.usp }}</p>
          </router-link>
        </div>
      </div>
      <div v-else>
        <p>No products found matching your search criteria.</p>
      </div>
    </div>
  </template>
  
  
  
  <style >
  .product-search-list {
    padding: 20px;
    text-align: center;
  }
  
  .product-cards {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); 
    gap: 20px;
    margin-top: 20px;
  }
  
  .product-card {
    border: 1px solid #ddd;
    border-radius: 8px;
    padding: 20px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    text-align: left;
    background-color: #fff;
  }
  
  .product-card h3 {
    font-size: 1.2em;
    color: #333;
  }
  
  .product-card p {
    color: #555;
    margin: 10px 0;
  }
  
  .product-price {
    font-weight: bold;
    color: #28a745;
  }
  
  .product-usp {
    font-style: italic;
    color: #777;
  }
  
  .product-image {
    width: 100%; 
    height: auto;
    border-radius: 8px;
    margin-bottom: 15px;
  }
  </style>
  