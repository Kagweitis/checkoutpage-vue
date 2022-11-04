<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Form from './components/Form.vue'
import Cart from './components/Cart.vue'
</script>

<template>

  <div class="container">
    <div class="payment-info">
        <Form />
    </div>
    
    <div class="order-summary">
      <Cart />
    </div>

  </div>

</template>

<style scoped>

  .container{
    width: 100%;
    display: flex;
    flex-direction: row;
    justify-content: space-between;
  }
  .payment-info{
    background-color: white;
    padding: 100px;
    box-shadow: 0 0 40px rgba(0,0,0,0.2);
    margin-right: 20px;
    flex-direction: column; 
    align-items: left;
    flex-basis: 40%;
    border-radius: 20px;
  }

  .order-summary{
    background-color: white;
    padding: 50px;
    box-shadow: 0 0 40px 0 rgba(0,0,0,0.2);
    flex-direction: column;
    flex-basis: 30%;
    border-radius: 20px;
    max-height: 500px;
  }

  

</style>
