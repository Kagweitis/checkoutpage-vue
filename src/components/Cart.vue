<script>
export default { 
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

        // methods: {

        // }
    }

}

</script>

<template>

    <div class="item-card">
        <li v-for="cart_item in cart_items">
            {{cart_item.item_name}}
            {{cart_item.item_price}}
        </li>
    </div>

</template>

<style scoped>
    .item-card{
        box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
        transition: 0.3s;
    }

    .item-card.hover{
        box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2);
    }

</style>