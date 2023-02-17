<template>
  <header>
    <div class="content">
      <div class="left">
        <router-link to="/">
          <div class="logo">
              <img src="img/Logo.svg" alt="Logo">
              <p>inance</p>
          </div>
        </router-link>
      </div>
      <div class="mid">
        <div class="hi">
          <h3>Hi, Rogers </h3>
        </div>
        <div class="searchbar">
          <img src="img/Search.svg" alt="Search">
          <input type="text" placeholder="Search">
        </div>
      </div>
      <div class="right">
        <div class="alert">
          <img src="img/Cloche.svg" alt="Alert">
          <span></span>
        </div>
        <div class="account">
          <img src="img/Account.png" alt="Account">
        </div>
      </div>
    </div>
  </header>
</template>

<script>

  export default {
    name : 'HeaderView',
  }

</script>

<style>

  header {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    height: 10vh;
    align-items: center;
    z-index: 99;
  }

  header .content {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 95%;
    align-items: center;
    margin: auto;
    height: 6vh;
  }

  header .left {
    display: flex;
    flex-direction: row;
    width: 20%;
  }

  header .left .logo {
    display: flex;
    flex-direction: row;
    align-items: flex-end;
  }

  header .left img {
    display: flex;
    width: 5.5vh;
    height: 5.5vh;
  }

  header .left .logo p{
    display: flex;
    color: #FFFFFF;
    font-weight: bold;
    font-size: 30px;
    margin-bottom: -1%;
  }

  header .mid {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 60%;
  }

  header .mid .hi {
    width: 40%;
    color: #FFFFFF;
    font-size: 25px;
    font-weight: 100;
  }

  header .mid .searchbar {
    display: flex;
    flex-direction: row;
    align-items: center;
    background-color: #FFFFFF;
    border-radius: 10px;
    height: 4vh;
    width: 48%;
    margin-left: 5vh;
  }

  header .mid .searchbar img{
    width: 3vh;
    height: 3vh;
    margin: 0 10px;
  }

  header .mid .searchbar input{
    border: none;
  }

  header .mid .searchbar input::placeholder{
    font-family: 'Inter', sans-serif;
    color: black;
    font-size: 16px;
  }

  header .mid .searchbar input:focus{
    outline: none;
    border: none;
  }

  header .right {
    display: flex;
    flex-direction: row;
    align-items: center;
    width: 30%;
    justify-content: space-between;
    height: 100%;
  }

  header .right .alert {
    display: flex;
    flex-direction: row;
    align-items: center;
    position: relative;
    height: 100%;
    width: 10%;
  }

  header .right .alert img {
    width: 4vh;
    height: 4vh;
  }

  header .right .alert img:hover {
    animation: bounce 0.5s ease-in-out infinite alternate;
  }

  @keyframes bounce {
    0% {
      transform: rotate(30deg);
    }
    100% {
      transform: rotate(-30deg);
    }
  }

  header .right .alert span {
    position: absolute;
    width: 1vh;
    height: 1vh;
    background-color: #6C1182;
    top: 3px;
    right: 3px;
    border-radius: 99px;
  }

  header .right .account {
    height: 100%;
  }

  header .right .account img {
    height: 100%;
  }

  @media screen and (max-width:767.98px) {

    header .left {
      width: 15%;
    }
    
    header .left .logo p{
      display: none;
    }

    header .mid {
      width: 60%;
      justify-content: start;
    }

    header .mid .hi h3{
      font-size: 12px;
      width: 100%;
    }

    header .mid .searchbar{
      width: 55%;
      margin-left: 0;
    }

    header .mid .searchbar input{
      width: 50%;
      font-size: 12px;
    }

    header .mid .searchbar input::placeholder{
      font-size: 12px;
    }

    header .right {
      width: 20%;
    }

    header .right .alert {
      width: 25%;
    }

    header .right .alert img{
      width: 100%;
    }

    header .right .alert span {
      width: 5px;
      height: 5px;
      position: absolute;
      top: 2px;
      right: -5px;
    }

    header .right .account {
      display: flex;
      align-items: center;
    }

    header .right .account img {
      width: 4vh;
      height: 4vh;
    }

  }

</style>
