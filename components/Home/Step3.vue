<template>
  <div class="container">
    <div class="text title mt-4 mb-3">Where's your place located?</div>
    <div class="text">
      Guesets will only get your exact address once they've booked a
      reservation.
    </div>
    <div class="location mt-4 mb-4">
      <img class="l-img" v-bind:src="location" alt="" />
      <div class="ml-3">Use current location</div>
    </div>
    <div class="l-address text mt-2"><span>or enter your address</span></div>
    <div>
      <div class="mt-4 mb-3">
        <div class="s-title mb-2">country/Region</div>
        <div class="">
          <b-form-select
            class="l-select"
            size="lg"
            v-model="selected"
            :options="options"
          ></b-form-select>
        </div>
      </div>
      <div class="s-title mb-2">Sreet address</div>
      <div class="s-title address mb-4">House name/number + street/road</div>
      <div class="s-title mb-2">Apt, suite. (optional)</div>
      <div class="s-title suite">Apt., suite, building access code</div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Step3",
  data() {
    return {
      location: require("../../assets/images/cursor.png"),
    };
  },
};
</script>
<style scoped>
.container {
  padding: 30px;
}
.title {
  font-size: 25px;
  font-weight: bold;
}
.text {
  line-height: 1;
  color: #464646;
}
.location {
  color: #018489;
  display: flex;
  border: #018489 solid 2px;
  justify-content: center;
  font-weight: bold;
  padding: 10px;
  border-radius: 3px;
}
.l-img {
  width: 17px;
}
.s-title {
  font-size: 20px;
  font-weight: 200;
}
.address {
  border: #ddbd3d solid 1px;
  border-radius: 2px;
  padding: 15px;
  background: #fef7e5;
}
.suite {
  border: #7c7b7b48 solid 1px;
  padding: 15px;
}
.l-select {
  height: 60px;
}
.l-address {
  width: 100%;
  text-align: center;
  border-bottom: #7c7b7b48 solid 1px;
  line-height: 0.1em;
  margin-top: 40px !important;
}
.l-address span {
  background: #fff;
  padding: 0 10px;
}
</style>
