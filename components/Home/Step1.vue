<template>
  <div class="container">
    <div class="title mt-4 mb-4">Let's get started listing your space</div>
    <div>STEP {{ step }}</div>
    <div class="title mt-2 mb-4">What kind of place do you have?</div>
    <div>
      <form>
        <div>
          <b-form-select
            v-model="selected"
            :options="options"
            class="mt-2 mb-2"
          ></b-form-select>
          <b-form-select
            v-model="selected"
            :options="options"
            class="mb-2"
          ></b-form-select>
          <b-form-input
            v-model="text"
            placeholder="Enter your name"
          ></b-form-input>
        </div>
        <div>
          <b-button size="md mt-3 btn">Continue</b-button>
        </div>
      </form>
    </div>
  </div>
</template>
<script>
export default {
  name: "Step1",
  emits: ["handle-next"],
  props: {
    step: Number,
  },
  data() {
    return {
      selected: null,
      options: [
        { value: null, text: "Please select an option" },
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
.title {
  font-size: 30px;
  color: #464646;
  line-height: 1;
}
.input {
  width: 100%;
  height: 38px;
  border-radius: 2px;
  margin-bottom: 5px;
}
.btn {
  background: #018489;
}
.container {
  padding: 30px;
}
</style>
