<template>
  <div class="s-container s-flex space-between mt-3">
    <div class="s-flex" v-on:click="$emit('handle-back')">
      <div class="s-img-container">
        <img class="s-img" v-bind:src="back" alt="" />
      </div>
      <div class="s-text">Back</div>
    </div>
    <div>
      <b-button
        :disabled="step === 4"
        @click="$emit('handle-next')"
        size="lg btn"
        >Next</b-button
      >
    </div>
  </div>
</template>
<script>
export default {
  name: "Sidemenu",
  emits: ["handle-next", "handle-back"],
  props: {
    step: Number,
  },
  data() {
    return {
      back: require("../../assets/images/left-chevron.png"),
    };
  },
};
</script>
<style scoped>
.s-container {
  background: white;
  box-shadow: 0px -3px 5px 0px #cecdcd34;
  padding: 30px;
  width: 100%;
  position: fixed;
  bottom: 0;
}
.btn {
  background: #018489;
}
.s-flex {
  display: flex;
}
.s-text {
  color: #018489;
}
.space-between {
  justify-content: space-between;
}
.s-img-container {
  width: 30px;
}
.s-img {
  width: 100%;
}
</style>
