<template>
  <div>
    <div class="img-container">
      <img class="img" v-bind:src="logo" alt="" />
    </div>
    <div v-if="step !== 1" class="progress bar">
      <div
        class="progress-bar"
        role="progressbar"
        :style="{ width: percent + '%', 'background-color': '#018489' }"
        aria-valuenow="step"
        aria-valuemin="1"
        aria-valuemax="6"
      ></div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Header",
  props: {
    step: Number,
    percent: Number,
  },
  data() {
    return {
      logo: require("../../assets/images/airbnb.png"),
      max: 6,
    };
  },
};
</script>
<style scoped>
.img-container {
  width: 100%;
  background: #f5f5f5;
  padding: 5px 0px 15px 18px;
}
img {
  width: 30px;
}
.bar {
  height: 10px;
}
</style>
