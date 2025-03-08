 <script>

  export default {
    data() {
      return {
        products: [
          {
            id: 1,
            name: "Product 1",
            price: 99.99,
            description: "This is a great product with amazing features.",
            usp: "Best value for money.",
            image: "https://via.placeholder.com/300x200?text=Product+1" 
          },
          {
            id: 2,
            name: "Product 2",
            price: 149.99,
            description: "A premium product that offers exceptional performance.",
            usp: "High durability and top quality.",
            image: "https://via.placeholder.com/300x200?text=Product+2" 
          },
          {
            id: 3,
            name: "Product 3",
            price: 49.99,
            description: "Affordable and reliable product for everyday use.",
            usp: "Great price for the value.",
            image: "https://via.placeholder.com/300x200?text=Product+3"
          },
          {
            id: 4,
            name: "Product 4",
            price: 199.99,
            description: "Top-tier product for professionals with specialized features.",
            usp: "Exceptional performance in all conditions.",
            image: "https://via.placeholder.com/300x200?text=Product+4"
          }
        ]
      };
    }
  };
  </script>

<template>
    <div class="product-list">
      <h2>Product List</h2>
      <div class="product-cards">
        <div v-for="product in products" :key="product.id" class="product-card">
          <img :src="product.image" alt="Product Image" class="product-image" />
          <h3 class="product-name">{{ product.name }}</h3>
          <p class="product-price">${{ product.price }}</p>
          <p class="product-description">{{ product.description }}</p>
          <p class="product-usp">USP: {{ product.usp }}</p>
        </div>
      </div>
    </div>
  </template>
  
 
  
  <style >
  .product-list {
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
  