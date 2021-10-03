<!--컴포지션API 반응형 데이터(반응성)-->
<template>
  <div @click="increase">
    {{ count }}
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    // 기본적으로는 반응성이 없는 상태 -> ref 필요 -> 객체데이터로 반환
    let count = ref(0);
    function increase() {
      count.value += 1;
    }

    return {
      count,
      increase,
    };
  },
};
</script>