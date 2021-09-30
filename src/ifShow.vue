<!--vue3-조건부렌더링-->
<template>
  <button @click="handler">Click me!</button>
  <!-- 
  <h1 v-if="isShow">Hello?!</h1>
  <h1 v-else-if="count > 3">Count > 3</h1>
  <h1 v-else>Good~</h1> 
  -->
  <!--template : 특정한 요소들을 그룹으로 만들때(최상위 template은 제외), v-if 가능 v-show 불가능-->
  <!--
  <template v-if="isShow">
    <h1>Title</h1>
    <p>Paragraph 1</p>
    <p>Paragraph 2</p>
  </template>
  -->
  <h1 v-show="isShow">Hello?!</h1>
  <!--v-if는 false인 경우 아예 렌더링되지 않음
  v-show는 false인 경우에도 렌더링되어 DOM에 남아있으며 display:none으로 설정
  변경이 잦으면 v-show, 별로 없으면 v-if-->
</template>

<script>
import template from "./template.vue";
export default {
  components: { template },
  data() {
    return {
      isShow: false,
      count: 0,
    };
  },
  methods: {
    handler() {
      this.isShow = !this.isShow;
      this.count += 1;
    },
  },
};
</script>