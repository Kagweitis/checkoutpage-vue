<script setup>
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://vuejs.org/api/sfc-script-setup.html#script-setup
import Form from './components/Form.vue'
import Card from './components/Card.vue'
import Cart from './components/Cart.vue'
</script>

<template>

  <div class="container">
    <div class="payment-info">
        <Card />
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
    margin-right: 20px;
    flex-direction: column; 
    align-items: left;
    flex-basis: 40%
  }

  .order-summary{
    flex-direction: column;
    color: red;
    flex-basis: 30%;
  }

  

</style>
