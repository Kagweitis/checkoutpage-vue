<script>
</script>

<template>
    <div class="form">
        <form action="submit">
            <label for="card-name">Card Name</label>
            <input type="text" name="card-name" id="card-name">

            <label for="card-number">Card Number</label>
            <input type="text" name="card-number" id="card-number">

            <label for="expiration">Expiration Date</label>
            <input type="text" name="expiration" id="expiration">

            <label for="cvc">CVC</label>
            <input type="text" name="cvc" id="cvc">
        </form>
    </div>
</template>

<style>
    input[type=text], select {
        width: 100%;
        padding: 12px 20px;
        margin: 8px 0;
        display: inline-block;
        border: 1px solid #ccc;
        border-radius: 6px;
        box-sizing: border-box;
    }
</style>
