<template>
  <div class="up">
    <div class="logo">
      <img :src="logo" alt="logo">
    </div>
    <div class="content">
      <div class="titre">
        <p>{{ titre }}</p>
        <p>{{ sousTitre }}</p>
      </div>
      <div class="others">
        <p>{{ money }}</p>
        <p>{{ date }}</p>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name : 'RecentView',

    props: {
      logo: String,
      titre: String,
      sousTitre: String,
      money: String,
      date: String,
    }
  }

</script>

<style scoped>

  div {
    width: 100%;
    height: 20%;
    display: flex;
    flex-direction: row;
    color: white;
    font-size: 16px;
  }

  div .logo {
    width: 15%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  div .logo img{
    width: 5vh;
    height: 5vh;
  }

  div .content {
    width: 80%;
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    margin-left: 3vh;
  }

  div .content .titre {
    display: flex;
    flex-direction: column;
    width: 40%;
    height: 100%;
    justify-content: center;
  }

  div .content .titre p:nth-child(2) {
    opacity: 70%;
  }

  div .content .others {
    display: flex;
    flex-direction: column;
    width: 35%;
    height: 100%;
    justify-content: center;
    color: #4AD619;
  }
  div .content .others p:nth-child(2) {
    opacity: 70%;
    color: white;
  }
    
</style>