<script>
  export default {
    data() {
      return {
        product: {} // Placeholder for the product data
      };
    },
    created() {
      const productId = this.$route.params.productId; 
      this.fetchProductDetails(productId); 
    },
    methods: {
      fetchProductDetails(id) {
    
        const mockProducts = [
          {
            id: 1,
            name: "Search Product 1",
            price: 99.99,
            description: "An affordable option for everyday use.",
            usp: "Great for daily tasks.",
            image: "https://via.placeholder.com/300x200?text=Search+Product+1"
          },
          {
            id: 2,
            name: "Search Product 2",
            price: 129.99,
            description: "A premium choice for professionals.",
            usp: "High-end features for top-tier performance.",
            image: "https://via.placeholder.com/300x200?text=Search+Product+2"
          }
        ];
  
        
        this.product = mockProducts.find(product => product.id === parseInt(id)) || {};
      },
      addToCart()
      {
        alert("Added to cart");
        //api call to move data to cart

      }
    }
  };
  </script>

<template>
    <h1 class="tittle">Decription</h1>
   <div class="product-description">
      
       <br>
     <div class="product-image-container">
       <img :src="product.image" alt="Product Image" class="product-image" />
     </div>
     <div class="product-details">
       <h2 class="product-name">{{ product.name }}</h2>
       <p class="product-price">${{ product.price }}</p>
       <p class="product-description-text">{{ product.description }}</p>
       <p class="product-usp">USP: {{ product.usp }}</p>
     </div>
     <div>
        <button @click="addToCart">Add To Cart</button>
     </div>
   </div>
 </template>

  <style >
 .tittle {
  display: block;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}

.product-description {
  display: flex;
  justify-content: center;
  align-items: flex-start;
  padding: 20px;
  gap: 30px;
  background-color: #f9f9f9;
}

.product-image-container {
  flex: 1;
  max-width: 400px;
}

.product-image {
  width: 100%;
  height: auto;
  border-radius: 8px;
  object-fit: cover;
}

.product-details {
  flex: 2;
  max-width: 600px;
}

.product-name {
  font-size: 2em;
  font-weight: bold;
  color: #333;
  margin-bottom: 10px;
}

.product-price {
  font-size: 1.5em;
  font-weight: bold;
  color: #28a745;
  margin-bottom: 20px;
}

.product-description-text {
  font-size: 1.1em;
  color: #555;
  line-height: 1.6;
  margin-bottom: 20px;
}

.product-usp {
  font-style: italic;
  color: #777;
  font-size: 1em;
}

</style>
