<template>
  <div class="item pb-4 pt-4">
    <div class="i-text">{{ text }}</div>
    <img class="i-image" v-bind:src="bullet" alt="" />
    <div class="line"></div>
  </div>
</template>

<script>
export default {
  name: "Item",
  props: {
    text: String,
  },
  data() {
    return {
      bullet: require("../../assets/images/bullet.png"),
    };
  },
};
</script>

<style scoped>
.item {
  display: flex;
  justify-content: space-between;
  border-bottom: #4646462c solid 1px;
}
.i-image {
  width: 40px;
  height: 40px;
  justify-self: flex-end;
}
.i-text {
  width: 80%;
}
</style>
