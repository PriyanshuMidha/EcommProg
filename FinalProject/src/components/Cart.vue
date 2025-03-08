<script>
import ThankYouPage from './ThankYouPage.vue'
export default {
    data()
    {
        return {}
    },
    methods: {
        checkoutButton()
        {
            this.$router.push('/ThankYou');
        }
    },
    components:{
       ThankYouPage
    },
    computed: {

    }

 
};

</script>
<template>
    <div>
        <h1> Orders</h1>
       <div>
        <h2>Product name</h2>
        <p>prodct price</p>
        <p>quantity</p>
       </div>

       <button @click="checkoutButton">Checkout</button>

    </div>

</template>