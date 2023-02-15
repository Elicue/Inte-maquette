<template>
  <div>
    <img :src="url" alt="logo">
    <p>{{ titre }}</p>
  </div>
</template>

<script>

  export default {
    name : 'ListElement',

    props: {
      url: String,
      titre: String,
    }
  }

</script>

<style scoped>
  div {
    display: flex;
    flex-direction: row;
    align-items: center;
  }

  div:hover {
    transform: scale(1.1);
    transition: ease-in-out 0.2s;
  }

  div img {
    width: 30px;
    height: 30px;
    margin-right: 2vh;
  }

  div p {
    color: white;
    opacity: 80%;
  }
</style>