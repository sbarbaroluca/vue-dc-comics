<template>
  <header class="container">
      <div id="logo-container">
        <img src="../assets/img/dc-logo.png" alt="dc comics logo" />
      </div>
      <nav>
        <ul>
          <li
            v-for="(link, index) in links"
            :key="index"
            :class="{ active: link.selected }"
           >
           <a :href="link.link">{{ link.text }}</a>
          </li> 
        </ul>
      </nav>    
  </header>
</template>

<script>
export default {
        name: "Header",
        data: function() {
          return {
            links: [
                {
                  text: "Characters",
                  link: "#characters",
                  selected: false
                },
                {
                  text: "Comics",
                  link: "#comics",
                  selected: true
                },
                {
                  text: "Movies",
                  link: "#movies",
                  selected: false
                },
                {
                  text: "Tv",
                  link: "#tv",
                  selected: false
                },
                {
                  text: "Games",
                  link: "#games",
                  selected: false
                },
                {
                  text: "Collectibles",
                  link: "#collectibles",
                  selected: false
                },
                {
                  text: "Videos",
                  link: "#videos",
                  selected: false
                },
                {
                  text: "Fans",
                  link: "#fans",
                  selected: false
                },
                {
                  text: "News",
                  link: "#news",
                  selected: false
                },
                {
                  text: "Shop",
                  link: "#shop",
                  selected: false
                },
            ]
          }
        }
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
@import "../style/mixins";
.container {
  @include flex-center("vertical");
  justify-content: space-between;
  overflow: hidden;
  img {
    padding: 10% 0;
    cursor: pointer;
  }
  nav {
    flex-grow: 1;
    ul {
      display: flex;
      justify-content: flex-end;
      li {
        margin-left: 2%;
        font-size: 13px;
        font-weight: 600;
        text-transform: uppercase;
        cursor: pointer;
        color: $genericTextColor;
        &.active {
          position: relative;
          color: $brandColor;
        }
        &.active::after {
          content: "";
          position: absolute;
          top: 65px;
          width: 100%;
          height: 20px;
          display: block;
          background: $brandColor;
          cursor: default;
        }
      }
    }
  }
}
</style>