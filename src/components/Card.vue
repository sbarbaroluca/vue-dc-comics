<template>
  <div class="card">
    <div class="img-container">
      <img :src="imgSrc" alt="" />
    </div>
    <h2>{{ series }}</h2>
  </div>
</template>

<script>
export default {
        name: "Card",
        props: {
          imgSrc: String,
          series: String
        }
};
</script>

<style lang="scss" scoped>
.card {
    width: calc(100% / 6 - 2%);
    margin: 3% 1%;
    cursor: pointer;
    .img-container {
      height: 200px;
      margin-bottom: 10%;
      overflow: hidden;
      & > img {
        width: 100%;
      }
    }
    h2 {
      font-size: 15px;
    }
}
</style>