<template>
  <div class="parent">
    <div class="content">
      <div class="haut">
        <div class="logo">
          <img :src="logo" alt="logo">
          <p>{{ titre }}</p>
        </div>
        <div class="bas">
          <p>{{oui}}</p>
          <p>{{non}}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

  export default {
    name : 'assetsView',

    props: {
      logo: String,
      titre: String,
      oui: String,
      non: String,
    }
  }

</script>

<style>

  .parent {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 40%;
    background: linear-gradient(98.73deg, #611D8D 35.75%, #2F7EC1 73.26%);
    color: white;
    border-radius: 15px;
  }

  .parent .content {
    display: flex;
    flex-direction: column;
    width: 90%;
    height: 85%;
    margin: auto;
  }

  .parent .content .haut {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    font-size: 16px;
  }

  .parent .content .haut .logo img{
    width: 5vh;
    height: 5vh;
  }

  .parent .content .bas {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    font-size: 20px;
  }

  @media screen and (max-width:767.98px) {

    .parent {
      padding: 10px 0 20px 0;
    }

    .parent .content .bas {
      font-size: 15px;
    }
}

</style>