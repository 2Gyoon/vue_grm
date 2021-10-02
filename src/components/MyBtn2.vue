<!--컴포넌트 속성상속 with components2-->
<template>
  <!-- template의 직계 자식요소 = 최상위요소, root 요소 -->
  <!-- 상속 : 컴포넌트가 사용되는 곳에 작성한 클래스나 기타 속성들이 컴포넌트 내부에 있는 하나의 요소에 연결되는 것 (최상위 요소가 하나일 때) -->
  <div class="btn">
    <slot></slot>
  </div>
  <h2 :class="$attrs.class" :style="$attrs.style"></h2>
  <!-- $attrs : 들어오는 속성들을 원하는 요소에 연결해줄 때 -->
  <h1 v-bind="$attrs"></h1>
</template>

<script>
export default {
  inheritAttrs: false,
  created() {
    console.log(this.$attrs);
  },
};
</script>

<style scoped>
.btn {
  display: inline-block;
  margin: 4px;
  padding: 6px 12px;
  border-radius: 4px;
  background-color: gray;
  color: white;
  cursor: pointer;
}
</style>