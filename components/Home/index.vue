<template>
  <div>
    <Header :step="step" :percent="percent" />
    <div v-if="step === 1"><Step1 :step="step" /></div>
    <div v-if="step === 2"><Step2 /></div>
    <div v-if="step === 3"><Step3 /></div>
    <div v-if="step === 4"><Step4 /></div>
    <Sidemenu
      @handle-next="handleNext"
      @handle-back="handleBack"
      :step="step"
    />
  </div>
</template>

<script>
import Header from "../Header";
import Step1 from "./Step1";
import Step2 from "./Step2";
import Step3 from "./Step3";
import Step4 from "./Step4";
import Sidemenu from "../Sidemenu";

export default {
  name: "Home",
  components: {
    Step1,
    Step2,
    Step3,
    Step4,
    Sidemenu,
    Header,
  },
  data() {
    return {
      step: 1,
      percent: 0,
    };
  },
  methods: {
    handleNext() {
      this.step++;
      this.percent = this.step / 0.06;
    },
    handleBack() {
      if (this.step > 1) {
        this.step--;
        this.percent = this.step / 0.06;
      }
    },
  },
};
</script>
