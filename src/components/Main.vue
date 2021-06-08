<template>
  <main>
    <div class="container">
      <h1>-->Content goes here &lt; --</h1>
    </div>
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
export default {
        name: "Main"
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
main {
  background: black;
  color: #fff;
  h1 {
    line-height: 100px;
  }
  .stores {
    height: 150px;
    background-color: $brandColor;
    .container {
      display: flex;
      justify-content: space-around;
      height: 100%;
      .store-link {
        display: flex;
        align-items: center;
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