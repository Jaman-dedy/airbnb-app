<template>
  <div class="container">
    <div class="text title mt-4 mb-4">
      How many guests can your place accomodate?
    </div>
    <div class="text">
      Check that you have enough beds to accommodate all your guests
      comfortably.
    </div>
    <div class="flex mt-4">
      <div>Guests</div>
      <img class="img" v-bind:src="minus" alt="" />
      <div>10</div>
      <img class="img" v-bind:src="plus" alt="" />
    </div>
    <div class="mt-5 mb-5">
      <div class="text s-title mb-3">How many bedrooms can guests use?</div>
      <div class="b-select">
        <b-form-select
          size="lg"
          v-model="selected"
          :options="options"
        ></b-form-select>
      </div>
    </div>
    <div class="mb-5">
      <div class="text mb-3 s-title">How many beds can guest use?</div>
      <div class="flex">
        <div>Beds</div>
        <img class="img" v-bind:src="minus" alt="" />
        <div>1</div>
        <img class="img" v-bind:src="plus" alt="" />
      </div>
    </div>
    <div>
      <div class="text sub-title mb-3">Sleeping arrangements</div>
      <div class="text">
        Sharing the types of beds in each room can help people understand the
        sleeping arrangements.
      </div>
    </div>
    <div class="line mt-4"></div>
  </div>
</template>
<script>
export default {
  name: "Step2",

  data() {
    return {
      plus: require("../../assets/images/plus.png"),
      minus: require("../../assets/images/minus.png"),
      selected: null,
      options: [
        { value: null, text: "Studio" },
        { value: "a", text: "This is First option" },
        { value: "b", text: "Selected Option" },
        { value: { C: "3PO" }, text: "This is an option with object value" },
        { value: "d", text: "This one is disabled", disabled: true },
      ],
    };
  },
};
</script>
<style scoped>
.text {
  line-height: 1;
  color: #464646;
}
.title {
  font-size: 26px;
  font-weight: bold;
}
.sub-title {
  font-size: 26px;
  font-weight: 200;
}
.s-title {
  font-size: 20px;
  font-weight: 200;
}
.container {
  padding: 30px;
}
.flex {
  display: flex;
  justify-content: space-between;
  width: 70%;
}
img {
  width: 30px;
}
.b-select {
  width: 70%;
}
.line {
  border-bottom: #46464649 solid 1px;
}
</style>
