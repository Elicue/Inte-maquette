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

  div img {
    width: 30px;
    height: 30px;
    margin-right: 10px;
  }

  div p {
    color: white;
    opacity: 80%;
  }
</style>