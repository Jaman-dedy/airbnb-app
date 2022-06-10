<template>
  <div class="container">
    <div class="mb-5 mt-4">
      <div class="title text">What amenities do you offer?</div>
      <div class="mt-2 text">
        These are just the amenities guests usually expect, bu you can add even
        more after you publish.
      </div>
    </div>
    <div>Essentials</div>
    <Item text="Towels, bed sheet, sop, toilet paper, and pillows" />
    <Item text="Wifi" />
    <Item text="TV" />
    <Item text="Heat" />
  </div>
</template>
<script>
import Item from "../Item";

export default {
  name: "Step4",
  components: {
    Item,
  },
  data: () => ({}),
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
</style>
