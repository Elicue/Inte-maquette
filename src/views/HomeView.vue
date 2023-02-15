<template>
  <Header/>
  <main>
    <div class="content">
      <div class="left">
        <div class="haut">
          <div class="dashboard">
            <div class="bg">
              <img src="img/dashboard.svg" alt="logo">
              <p>Dashboard</p>
            </div>
          </div>
          <div class="list">
            <listElement titre="Invoices" url="img/invoice.svg"/>
            <listElement titre="Clients" url="img/people.svg"/>
            <listElement titre="Products" url="img/box.svg"/>
            <listElement titre="Messages" url="img/invoice.svg"/>
            <listElement titre="Settings" url="img/message.svg"/>
            <listElement titre="Help" url="img/infos.svg"/>
          </div>
        </div>
        <div class="logout">
          <listElement titre="Log Out" url="img/Logout.svg"/>
        </div>
      </div>
      <div class="mid">
        <div class="haut">
          <div class="left">
            <p>Total Balance </p>
            <div class="mid">
              <p>0.97894652 </p>
              <span>BTC</span>
            </div>
            <p>$40,123.56</p>
          </div>
          <div class="right">
            <p>Portfolio</p>
            <p>Funding</p>
            <p>Assets</p>
            <p>P2P</p>
          </div>
        </div>
        <div class="centre">
          <img src="img/graph.png" alt="graph">
        </div>
        <div class="bottom">
          <div class="haut">
            <p>Recent Transactions</p>
            <p>See all coins</p>
          </div>
          <div class="bottom">
            <transaction logo="img/Bitcoin_.svg" titre="Bitcoin" sousTitre="BTC" vague="img/vague.svg" />
            <transaction logo="img/Etherum.svg" titre="Etherum" sousTitre="ETH" vague="img/vagueB.svg" />
          </div>
        </div>
      </div>
      <div class="right">
        <div class="top">
          <h3>Recent Transactions </h3>
          <recent logo="img/usdt.svg" titre="Usdt" sousTitre="Received" money="+$3,546" date="Today, 13:45 pm"/>
          <recent logo="img/bnb.svg" titre="BNB" sousTitre="Buy" money="+ 0.7546" date="Today, 5:45 am"/>
          <recent logo="img/LiteCoin.svg" titre="Lite Coin" sousTitre="Withdrawal" money="+ 0.7546" date="Today 7:55 am"/>
          <recent logo="img/Bitcoin.svg" titre="Bitcoin" sousTitre="Received" money="+$2,7546" date="Today, 8:55 am"/>
          <recent logo="img/etherum.svg" titre="Etherum" sousTitre="Received" money="+$1.646" date="Today, 10:02 am"/>
        </div>
        <div class="bottom">
          <h3>Assets</h3>
          <assets titre="Bitcoin" logo="img/BitcoinB.svg" oui="121,6450.45" non="BTC"/>
          <assets titre="Etherum" logo="img/etherum.svg" oui="143,850.45" non="ETH"/>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Header from '@/components/header.vue'
import listElement from '@/components/listElement.vue'
import transaction from '@/components/transaction.vue'
import assets from '@/components/assets.vue'
import recent from '@/components/recent.vue'


export default {
  name: 'HomeView',
  components: {
    Header,
    listElement,
    transaction,
    assets,
    recent
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: 'Poppins', sans-serif;
    text-decoration: none;
  }

  body {
    background-color: black;
  }

  main {
    width: 100%;
    display: flex;
    flex-direction: row;
    height: 90vh;
  }

  main .content {
    width: 95%;
    height: 95%;
    margin: auto;
    display: flex;
    flex-direction: row;
  }

  /*-------------------------------LEFT--------------------------------------------*/

  main .content .left {
    height: 100%;
    display: flex;
    flex-direction: column;
    width: 18%;
    justify-content: space-between;
    padding-top: 8vh;
  }

  main .content .left .haut {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    height: 60%;
  }

  main .content .left .haut .dashboard {
    display: flex;
    flex-direction: row;
    width: 100%;
    height: 15%;
  }

  main .content .left .haut .dashboard .bg {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding: 8px 20px;
    border-radius: 10px;
    justify-content: space-between;
    background: linear-gradient(266.37deg, #FAFF00 -5.82%, #FAFF00 15.95%, #1970D6 41.2%, #6C1182 72.88%);
  }

  main .content .left .haut .dashboard .bg img{
    width: 30px;
    height: 30px;
  }

  main .content .left .haut .dashboard .bg p{
    margin-left: 10px;
  }

  main .content .left .haut .list {
    display: flex;
    flex-direction: column;
    width: 100%;
    height: 70%;
    justify-content: space-between;
    margin-left: 2vh;
  }

  main .content .left .logout {
    margin-left: 2vh;
  }

  @media screen and (max-width:767.98px) {
    
    main .content .left {
      display: none;
    }

  }


  /*-------------------------------LEFT--------------------------------------------*/
  /*-------------------------------MID--------------------------------------------*/
  /*-------------------------------MID-HAUT--------------------------------------------*/

  main .content .mid {
    height: 100%;
    width: 52%;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }

  main .content .mid .haut {
    display: flex;
    flex-direction: row;
    height: 13%;
    width: 80%;
    align-items: center;
  }

  main .content .mid .haut .left {
    display: flex;
    flex-direction: column;
    width: 30%;
    padding-top: 0;
    justify-content: left;
  }

  main .content .mid .haut .left p{
    color: #FFFFFF;
    opacity: 80%;
    font-weight: 900;
    font-size: 16px;
  }

  main .content .mid .haut .left p:nth-child(3){
    opacity: 70%;
  }

  main .content .mid .haut .left .mid {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  main .content .mid .haut .left .mid p{
    color:#FFFFFF;
    font-weight: 900;
    font-size: 22px;
    opacity: 100%;
  }

  main .content .mid .haut .left .mid span{
    color:black;
    background-color: #FAFF00;
    font-size: 13px;
    padding: 0.2rem 0.5rem;
    border-radius: 8px;
    margin-left: 2vh;
    font-weight: bold;
  }

  main .content .mid .haut .right {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
    align-items: center;
    width: 55%;
    height: 50%;
    background: #292727;
    color: white;
    border-radius: 10px;
    padding: 0 0.5rem;
  }

  main .content .mid .haut .right p{
    display: flex;
    width: 25%;
    text-align: center;
    align-items: center;
    justify-content: center;
  }

  main .content .mid .haut .right p:hover{
    background-color: #0D0C0C;
    padding: 0.5rem 0.5rem;
    border-radius: 7px;
    transform: scaleY(1.1);
    transition: ease-in-out 0.2s;
  }

  @media screen and (max-width:767.98px) {
    
    main .content .mid {
      width: 100%;
      height: 100%;
    }

    main .content .mid .haut {
      width: 100%;
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      height: 30%;
    }

    main .content .mid .haut .left{
      width: 50%;
    }

    main .content .mid .haut .right{
      width: 98%;
      padding: 0;
      margin-top: 2vh;
    }

  }


  /*-------------------------------MID-HAUT--------------------------------------------*/
  /*-------------------------------MID-MID--------------------------------------------*/

  main .content .mid .centre {
    display: flex;
    width: 100%;
    height: 55%;
    margin-top: 2vh;
  }

  main .content .mid .centre img{
    width: 100%;
    height: 100%;
  }

  @media screen and (max-width:767.98px) {
      
    main .content .mid .centre {
      display: flex;
      width: 100%;
      height: 35%;
    }
  }

  /*-------------------------------MID-MID--------------------------------------------*/
  /*-------------------------------MID-BOTTOM--------------------------------------------*/

  main .content .mid .bottom {
    display: flex;
    width: 97%;
    height: 27%;
    flex-direction: column;
    margin: auto;
  }

  main .content .mid .bottom .haut{
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    width: 100%;
    height: 20%;
    align-items: center;
    color: white;
    font-size: 20px;
    font-weight: bold;
  }

  main .content .mid .bottom .haut p:nth-child(2){
    opacity: 70%;
  }

  main .content .mid .bottom .bottom{
    display: flex;
    flex-direction: columns;
    width: 100%;
    height: 80%;
  }

  main .content .mid .bottom .bottom .parent:nth-child(2) .market p:nth-child(2){
    color: #6C1182;
  }

  main .content .mid .bottom .bottom .parent:nth-child(2) .h p:nth-child(2){
    color: #D61919;
  }

  @media screen and (max-width:767.98px) {
      
    main .content .mid .bottom {
      display: flex;
      width: 100%;
      height: 35%;
      flex-direction: column;
      margin: auto;
      margin-top: 3vh;
    }

    main .content .mid .bottom .haut {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      width: 100%;
      align-items: center;
      color: white;
      font-size: 15px;
      font-weight: bold;
    }

    main .content .mid .bottom .bottom{
      display: flex;
      flex-direction: column;
      width: 100%;
      height: 100%;
      justify-content: space-between;
    }

    main .content .mid .bottom .bottom .parent:nth-child(2){
      margin-top: 2vh;
    }
  }

  /*-------------------------------MID-BOTTOM--------------------------------------------*/
  /*-------------------------------MID--------------------------------------------*/
  /*-------------------------------RIGHT--------------------------------------------*/

    main .content .right {
      height: 100%;
      width: 25%;
      margin: auto;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    @media screen and (max-width:767.98px) {
      
      main .content .right {
        display: none;
      }

    }


  /*-------------------------------RIGHT-HAUT--------------------------------------------*/

    main .content .right .top{
      height: 55%;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    main .content .right .top h3{
      font-size: 25px;
      color: white;
      margin-bottom: 2vh;
    }

    main .content .right .top .up:nth-child(4) .others  p:nth-child(1){
      color: #D61919;
    }
  
  /*-------------------------------RIGHT-HAUT--------------------------------------------*/

  /*-------------------------------RIGHT-BOTTOM--------------------------------------------*/

    main .content .right .bottom{
      height: 42%;
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }

    main .content .right .bottom h3 {
      font-size: 25px;
      color: white;
    }

    main .content .right .bottom .parent:nth-child(3){
      background: linear-gradient(99.56deg, #FAFF00 35.82%, #29ABE2 64.75%, rgba(255, 255, 255, 0.7) 91.33%);
      color: black;
    }

  /*-------------------------------RIGHT-BOTTOM--------------------------------------------*/
  /*-------------------------------RIGHT--------------------------------------------*/

</style>

