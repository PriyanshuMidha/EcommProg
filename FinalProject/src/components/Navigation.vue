<script>
import Cart from './Cart.vue'
import Profile from './Profile.vue'
import Home from './Home.vue'
export default {
    data()
    {
        return {}
    },
    methods: {
        goToCart()
        {
            this.$router.push('/Cart');
        },
        goToProfile()
        {
            this.$router.push('/Profile');
        },
        homePage()
        {
            this.$router.push('/');   
        },
        
        toggleSearch() {
            this.showSearch = !this.showSearch;  
            this.$router.push('/ProductSearchList' );
        }

    },
    components:{
        Cart,Profile,Home
    },
    computed: {

    }

 
};
</script>

<template>
    <nav class="navbar">
      <ul class="navbar-list">
        <li  class="navbar-item logo"><button  @click="homePage">Logo </button></li>
        <li class="navbar-item search-container">
          <input type="text" class="search-input" placeholder="Search">
          <button class="search-button" @click="toggleSearch" >Search</button>
        </li>
        <li class="navbar-item cart-profile">
          <button class="cart" @click="goToCart">Cart</button>
          <button class="profile" @click="goToProfile">Profile</button>
        </li>
      </ul>
    </nav>
  </template>
  
 
  
  <style scoped>
  .navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    background-color: #333;
    padding: 10px 0;
    z-index: 1000;
  }
  
  .navbar-list {
    display: flex;
    list-style-type: none;
    margin: 0;
    padding: 0 20px;
    width: 100%;
    justify-content: space-between;
  }
  
  .navbar-item {
    color: white;
    font-size: 16px;
    display: flex;
    align-items: center;
    margin-right: 20px; 
  }
  
  .logo {
    flex: 0 1 auto; 
  }
  
  .search-container {
    flex: 0 1 auto;
    display: flex;
    align-items: center;
  }
  
  .search-input {
    padding: 5px;
    margin-right: 10px;
    border: none;
    border-radius: 4px;
    width: 500px; 
  }
  
  .search-button {
    padding: 5px 10px;
    background-color: #555;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  .search-button:hover {
    background-color: #777;
  }
  
  .cart-profile {
    flex: 0 1 auto; 
  
  }
  .cart{
    margin:5px
  }
  </style>
  