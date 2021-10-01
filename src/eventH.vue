<!--이벤트 핸들링-->
<template>
  <!--
  <button @click="handler('hi', $event)">Click me 1</button>
  <button @click="handler('what', $event)">Click me 2</button>
  -->
  <button @click="handlerA(), handlerB()">Click me!</button>
  <!-- 하나의 요소에 들어가는 이벤트가 여러개라면 쉼표로 구분하고 ()를 꼭 써주기 -->
</template>

<script>
export default {
  /*
  methods: {
    handler(msg, event) {
      console.log(msg);
      console.log(event);
    },
  }
  */
  methods: {
    handlerA() {
      console.log("A");
    },
    handlerB() {
      console.log("B");
    },
  },
};
</script>