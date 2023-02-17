<template>
  <div class="parent">
    <div class="first">
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
    </div>
    <div class="second">
      <div class="vague">
        <img :src="vague" alt="vague">
      </div>
      <div class="btn">
        <button>Trade</button>
      </div>
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

  .parent .first {
    width: 60%;
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  .parent .second {
    width: 40%;
    display: flex;
    flex-direction: row;
    align-items: center;
  }
  
  .blanc {
    color: white;
  }
  .parent .logo {
    width: 15%;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .parent .logo img {
    width: 30px;
    height: 30px;
  }

  .parent .titre {
    width: 20%;
    color: white;
  }

  .parent .titre p:nth-child(2){
    color: white;
    opacity: 70%;
  }

  .parent .market {
    width: 32%;
  }

  .parent .market p:nth-child(2){
    color: #1970D6;
  }

  .parent .h {
    width: 32%;
  }
  
  .parent .h p:nth-child(2){
    color: #4AD619;
  }

  .parent .vague {
    width: 70%;
    display: flex;
    align-items: center;
  }

  .parent .vague img {
    width: 70%;
  }

  .parent .btn {
    width: 30%;
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

  @media screen and (max-width:767.98px) {
    .parent {
      display: flex;
      flex-direction: column;
      width: 100%;
      height: 100%;
      padding: 2vh 0;
    }
    .parent .first {
      width: 100%;
      display: flex;
      flex-direction: row;
      align-items: center;
    }
    .parent .second {
      width: 80%;
      display: flex;
      flex-direction: row;
      align-items: center;
      margin-top: 2vh;
    }
  }

</style>