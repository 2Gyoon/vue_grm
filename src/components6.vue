<!--컴포넌트 Refs with Hello-->
<template>
  <!-- ref : reference / mounted에서 사용 가능-->
  <!-- <h1 ref="hello">Hello world!</h1> -->
  <Hello ref="hello" />
</template>

<script>
import Hello from "~/components/Hello";
export default {
  components: {
    Hello,
  },
  mounted() {
    console.log(this.$refs.hello.$refs.good);
    // $el 속성 적어줘야 해당하는 내용을 참조할 수 있음
  },
};
</script>