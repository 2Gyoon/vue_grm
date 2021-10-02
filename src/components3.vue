<!--컴포넌트 emit with MyBtn3-->
<template>
  <MyBtn @2gyoon="log" @change-msg="logMsg"> Banana </MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn3";

export default {
  components: {
    MyBtn,
  },
  methods: {
    log(event) {
      console.log("Click!!");
      console.log(event);
    },
    logMsg(msg) {
      console.log(msg);
    },
  },
};
</script>