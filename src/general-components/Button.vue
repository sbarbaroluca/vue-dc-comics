<template>
  <div class="button">{{ text }}</div>
</template>

<script>
export default {
        name: "Button",
        props: {
          text: String
        }
};
</script>

<style lang="scss" scoped>
@import "../style/variables";
.button {
  padding: 10px 50px;
  background-color: $brandColor;
  text-transform: uppercase;
  font-size: 14px;
  font-weight: 600;
}
</style>