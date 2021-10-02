<!--컴포넌트 provide, inject with Parent & Child-->
<template>
  <button @click="message = 'Good?'">Click!</button>
  <h1>App: {{ message }}</h1>
  <Parent />
</template>

<script>
import Parent from "~/components/Parent";
import { computed } from "vue";

export default {
  components: {
    Parent,
  },
  data() {
    return {
      message: "Hello world!",
    };
  },
  // provide : 반응성x
  provide() {
    return {
      msg: computed(() => this.message),
    };
  },
};
</script>