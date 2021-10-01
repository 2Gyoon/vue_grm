<!--이벤트 핸들링-이벤트 수식어-->
<!--이벤트 버블링과 캡쳐링 => @click.stop="handlerB" / @click.capture="handlerA"-->
<!--@click.self : target(실제로 클릭한 부분)과 currentTarget(이벤트가 연결되어 있는 요소)가 같은 경우에만 동작하도록 하는 수식어-->
<template>
  <!-- 
  <a href="http://naver.com" target="_blank" @click.prevent.once="handler">
    NAVER
  </a> 
  -->
  <!-- @click.prevent / @click.once -->
  <!--
  <div
    class="parent"
    @click.self="handlerA">
    <div
      class="child"
      style=">
    </div>
  </div>
  -->
  <!--@wheel.passive : 로직의 처리와 화면을 독립시켜줄 수 있음, 부하를 줄여줌-->
  <div class="parent" @wheel.passive="handler">
    <div class="child"></div>
  </div>
</template>

<script>
export default {
  methods: {
    /*
    handler() {
      // event.preventDefault();
      console.log("ABC!");
    },
    */
    /*
    handlerA(event) {
      console.log(event.target)
      console.log(event.currentTarget)
      console.log("A");
    },
    handlerB() {
      // event.stopPropagation()
      console.log("B");
    },
    */
    handler(event) {
      for (let i = 0; i < 10000; i += 1) {
        console.log(event);
      }
    },
  },
};
</script>


<style lang="scss" scoped>
.parent {
  width: 200px;
  height: 100px;
  background-color: royalblue;
  margin: 10px;
  padding: 10px;
  overflow: auto;
  .child {
    width: 100px;
    // height: 100px;
    height: 2000px;
    background-color: orange;
  }
}
</style>