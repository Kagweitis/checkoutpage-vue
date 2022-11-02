<script>
import Card from './Card.vue'


export default {
  components: {
   Card
  },
  data(){
    return{
        name: "",
        card_number: "",
        expiry: ""
    }
},
watch: {
    card_number() {
      // Card number without dash (-)
        let realNumber = this.card_number.replace(/-/gi, '')
        
        // Generate dashed number
        let dashedNumber = realNumber.match(/.{1,4}/g)

        // Replace the dashed number with the real one
        this.card_number = dashedNumber.join('-')
    }
  }
}
</script>

<template>
    <head>
        <!-- <link rel="preconnect" href="https://fonts.googleapis.com">
        <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
        <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500&display=swap" rel="stylesheet"> -->
    </head>

    <Card :name="name"
          :card_number="card_number"
          :expiry="expiry"/>
    
    <form action="submit">
        <div class="flex">
            <label for="card-name">Name on Card</label>
            <input type="text" name="card-name" id="card-name" v-model="name"> 

            <label for="card-number">Card Number</label>
            <input type="text" name="card-number" id="card-number" maxlength="19" v-model="card_number">
            <!-- pattern="[,0-9]*" -->

            <label for="expiration">Expiration Date</label>
            <input type="text" name="expiration" id="expiration" v-model="expiry">

            <label for="cvc">CVC</label>
            <input type="text" name="cvc" id="cvc">

            Total: {{}}
            

            <button>Confirm Payment</button>
        </div>
    </form>
</template>

<style scoped>
    @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600&display=swap');
    input[type=text], select {
        width: 100%;
        padding: 12px 20px;
        margin: 8px 0;
        /* display: inline-block; */
        border: 1px solid #ccc;
        border-radius: 6px;
        box-sizing: border-box;
    }

    label{
        display: inline-block;
        text-align: left;
    }

    .flex{
        display: flex;
        flex-direction: column;
        flex: 1;
        /* align-items: left; */
        font-family: 'Quicksand', sans-serif;
        font-weight: 800;
    }
</style>
