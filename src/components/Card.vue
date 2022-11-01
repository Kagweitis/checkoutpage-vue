<script>
export default {
  name: 'Card',
  props: {
    name: String,
    card_number: String,
    expiry: String,
  },
}

</script>

<template>
  <!-- <img src="../assets/img/ncba card.png" alt="card image"> -->
<div class="cont">
  <h3>Payment Information</h3>
  <div class="card">
    
    <div class="header">
      <div>
        <img class="chip" src="https://raw.githubusercontent.com/muhammederdem/credit-card-form/master/src/assets/images/chip.png" alt="chip" style="height:50px; ">
      </div>
      <div>
        <img class="logo" src="../assets/img/logo-removebg-preview.png" alt="logo" style="height:50px;
        padding: 20px;">  
      </div>
    </div>


      <p style="text-align: center; color: aliceblue; font-size: large; width: 100%;">{{ card_number || '#### #### #### ####' }}</p>
      <div class="card-details">
        <div>
          <p style="color: aliceblue;">
            CARD HOLDER    
          </p>
          <p style="color: aliceblue; font-weight: bold;">{{ name || 'Full Name' }} </p> 
        </div>
        <div class="expiry">
          <P style="color: aliceblue;"> EXPIRY DATE </P>
          <p style="color: aliceblue; font-weight: bold;">{{ expiry || 'MM/YY' }}</p>
        </div>   
      </div>


  </div>
</div>
</template>

<style scope>
  /* img{
    box-shadow: 0 0 40px darkgray;
      
  } */

  @import url('https://fonts.googleapis.com/css2?family=Quicksand:wght@300;400;500;600&display=swap');

  .card{
    width: 80%;
    /* height: 10%; */
    /* background: linear-gradient(90deg, #00d2ff 0%, #3a47d5 100%); */
    background-image: url("../assets/img/attempt1.jpg");
    margin-bottom: 30px;
    box-shadow: 0 0 40px rgb(146, 204, 224);
    border-radius: 20px;
  }
  img{
    display: flex;
    flex-direction: column;
    size: 10%;
  }

  .logo{
    size: 10px;
  }

  .cont{
    font-family: 'Quicksand', sans-serif;
  }

  .p{
    font-size: x-small;
  }

  .card-details{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    }

    .header{
      display: flex;
      flex-direction: row;
      justify-content: space-between;
    }



  
 
</style>
