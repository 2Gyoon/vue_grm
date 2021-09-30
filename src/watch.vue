<!--vue3-watch-->

<template>
  <h1 @click="changeMessage">
    {{ msg }}
  </h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello?",
    };
  },
  computed: {
    reversedMessage() {
      return this.msg.split("").reverse().join("");
    },
  },
  watch: {
    // 특정한 데이터가 변경되는 것을 감시해서 추가적인 로직을 만들어 줄 때 사용(계산된 데이터도 감시가능)
    msg(newValue) {
      console.log("msg:", newValue);
    },
    reversedMessage() {
      console.log("reversedMessage:", this.reversedMessage);
    },
  },
  methods: {
    changeMessage() {
      this.msg = "Good!";
    },
  },
};
</script>

<style>
h1 {
  font-size: 50px;
  color: royalblue;
}
</style>