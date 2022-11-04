
<script>
    export default {
        data(){
            return{
                
            }
        },
        props: ['id'],
        emits: ['deleteItem'],
        methods: {
            passId(){
                this.$emit('deleteItem', { id: this.id })
            }
        }
       
    }
</script>


<template>
    <head>
        <!-- <link rel="stylesheet" src="https://kit.fontawesome.com/c3fc2fc6d6.js" crossorigin="anonymous"> -->
    </head>
    <div>
        <button  class="delete" @click="$emit('deleteItem', id)"
         type="button">x</button>
    </div>
</template>

<style>

    .container{
        display: flex;
        flex-direction: row;
        align-content: left;
    }
    .delete{
        color: aliceblue;
        background-color: rgb(120, 120, 236);
        padding: 0;
    }

    .delete:hover{
        border: none;
    }
    .delete:focus{
        outline: none;
    }
</style>
