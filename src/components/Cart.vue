<script>
import Delete from './Delete.vue'
export default { 
    name: "Cart",
    components: {
        Delete,
    },
    data() {
        return{
            cart_items : [
                {
                    item_name: 'bike',
                    item_price: '$1000'
                },

                {
                    item_name: 'pump',
                    item_price: '$300'
                },

                {
                    item_name: 'helmet',
                    item_price: '$100'
                },

            ]
        }
    },
    methods: {
        deleteItem(index) {
            console.log('deleted')
            this.items.splice(index, 1)
    },

    }
}

</script>

<template>
<div id="container">
    <div class="heading">
        <h3>Order Summary</h3>
    </div>
    <div class="item-card">
        <li class="item" v-for="cart_item in cart_items"
        @deleteItem="deleteItem(index)">
            {{cart_item.item_name}}
            {{cart_item.item_price}}
            <Delete />
            
        </li>
    </div>
</div>

</template>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600&display=swap');

  #container{
    font-family: 'Quicksand', sans-serif;
    font-weight: 800;
    padding-top: 50px;
  }

  .header{
   margin-top: 100px;
  }

    /* .item-card{
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        font-family: 'Quicksand', sans-serif;
        font-weight: 800;
    } */

    .item{
        width: 40%;
        top: 50%;
        left: 50%;
        background: rgb(120, 120, 236);
        border-radius: 10px;
        min-width: 400px;
        padding: 20px;
        margin: 20px;
        color: aliceblue;
        /* position: absolute; */
        min-height: 100px;
        /* transform: translate(-50%,-50%); */
        list-style: none;
        font-family: 'Quicksand', sans-serif;
        font-weight: 800;
    }

    /* .item-card.hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    } */

</style>