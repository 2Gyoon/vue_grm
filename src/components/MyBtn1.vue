<!--컴포넌트 기초 with components1-->
<template>
  <div
    :class="{ large: large }"
    :style="{ backgroundColor: color }"
    class="btn"
  >
    <slot></slot>
    <!-- slot : 단순히 텍스트만 받는 것이 아닌 열리고 닫히는 태그 사이에 있는 모든 내용을 이 부분에 대체해서 넣어준다-->
  </div>
</template>

<script>
export default {
  // 부모 자식간의 데이터 통신
  props: {
    color: {
      type: String,
      default: "gray",
    },
    large: {
      type: Boolean,
      default: false,
    },
    /*
    text: {
      type: String,
      default: "",
    },
    */
  },
};
</script>

<style scoped lang="scss">
.btn {
  display: inline-block;
  margin: 4px;
  padding: 6px 12px;
  border-radius: 4px;
  background-color: gray;
  color: white;
  cursor: pointer;
  &.large {
    font-size: 20px;
    padding: 10px 20px;
  }
}
</style>
