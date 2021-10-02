<!--컴포넌트 속성상속 with MyBtn2-->
<template>
  <MyBtn class="2gyoon" style="color: red" title="Hello world!"> Banana </MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn2";
export default {
  components: {
    MyBtn,
  },
};
</script>