<template>
  <main>
    <Jumbotron />
    <Comics />
    <div class="container"></div>
    <div class="stores">
      <div class="container">
        <div class="store-link">
          <img src="../assets/img/buy-comics-digital-comics.png" alt="digital comics" />
          <span>Digital comics</span>
        </div>
        <div class="store-link">
          <img src="../assets/img/buy-comics-merchandise.png" alt="DC merchandise" />
          <span>DC Merchandise</span>
        </div>
        <div class="store-link">
          <img src="../assets/img/buy-comics-subscriptions.png" alt="subscription" />
          <span>Subscription</span>
        </div>
        <div class="store-link">
          <img src="../assets/img/buy-comics-shop-locator.png" alt="comic shop locator" />
          <span>Comic shop locator</span>
        </div>
        <div class="store-link">
          <img src="../assets/img/buy-dc-power-visa.svg" alt="DC power visa" />
          <span>DC power visa</span>
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import Jumbotron from "./Jumbotron.vue";
import Comics from "./Comics.vue";
export default {
        name: "Main",
        components: {
          Jumbotron,
          Comics
        }
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
@import "../style/mixins";
main {
  background: black;
  color: #fff;
  h1 {
    line-height: 150px;
  }
  .stores {
    height: 150px;
    background-color: $brandColor;
    .container {
      display: flex;
      justify-content: space-around;
      height: 100%;
      .store-link {
        @include flex-center("vertical");
        width: 20%;
        &:last-child > img {
          height: 25%;
        }
        img {
          height: 35%;
          margin: 0 8%;
        }
        span {
          font-size: 14px;
          text-transform: uppercase;
        }
      }
    }
  }
}
</style>