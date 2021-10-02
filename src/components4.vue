<!--컴포넌트 slot with MyBtn4-->
<template>
  <MyBtn>
    <template #icon>
      <span>(B)</span>
    </template>
    <template #text>
      <span>Banana</span>
    </template>
  </MyBtn>
</template>

<script>
import MyBtn from "~/components/MyBtn4";
export default {
  components: {
    MyBtn,
  },
};
</script>