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
    </div>
  </main>
</template>

<script>
import Header from '@/components/header.vue'
import listElement from '@/components/listElement.vue'

export default {
  name: 'HomeView',
  components: {
    Header,
    listElement,
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

  /*-------------------------------LEFT--------------------------------------------*/

</style>

