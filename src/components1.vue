<!--컴포넌트 기초 with MyBtn1.vue-->
<template>
  <MyBtn>Banana</MyBtn>
  <MyBtn :color="color">
    <span style="color: red">Orange</span>
  </MyBtn>
  <MyBtn large color="royalblue">Apple</MyBtn>
  <MyBtn>Cherry</MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn1";

export default {
  components: {
    MyBtn,
  },
  data() {
    return {
      color: "#000",
    };
  },
};
</script>