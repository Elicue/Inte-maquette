<template>
  <div class="parent">
    <div class="logo">
      <img :src="logo" alt="logo">
    </div>
    <div class="titre">
      <p class="blanc">{{ titre }}</p>
      <p class="blanc">{{ sousTitre }}</p>
    </div>
    <div class="market">
      <p>Market Cap</p>
      <p>$40,243.70</p>
    </div>
    <div class="h">
      <p>24h change</p>
      <p>+1,56</p>
    </div>
    <div class="vague">
      <img :src="vague" alt="vague">
    </div>
    <div class="btn">
      <button>Trade</button>
    </div>
  </div>
</template>

<script>

  export default {
    name : 'TransactionView',

    props: {
      logo: String,
      titre: String,
      sousTitre: String,
      vague: String,
    }
  }

</script>

<style scoped>

  .parent {
    background: rgba(32, 35, 43, 0.7);
    width: 98%;
    margin: auto;
    display: flex;
    flex-direction: row;
    border-radius: 20px;
    color: white;
    align-items: center;
    height: 7vh;
    /* box-shadow: 0px 0px 25px #464a52; */
  }

  .blanc {
    color: white;
  }
  .parent .logo {
    width: 10%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .parent .logo img {
    width: 30px;
    height: 30px;
  }

  .parent .titre {
    width: 12%;
    color: white;
  }

  .parent .titre p:nth-child(2){
    color: white;
    opacity: 70%;
  }

  .parent .market {
    width: 20%;
  }

  .parent .market p:nth-child(2){
    color: #1970D6;
  }

  .parent .h {
    width: 20%;
  }
  
  .parent .h p:nth-child(2){
    color: #4AD619;
  }

  .parent .vague {
    width: 25%;
  }

  .parent .btn {
    width: 10%;
  }

  .parent .btn button {
    background-color: #000000;
    border: none;
    border-radius: 90px;
    color: white;
    padding: 0.5rem 1rem ;
  }
  
  .parent .btn button:hover {
    transform: scale(1.1);
    transition: ease-in-out 0.2s;
  }
</style>