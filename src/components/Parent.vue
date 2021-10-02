<!--컴포넌트 provide, inject with components5-->
<template>
  <Child />
</template>

<script>
import Child from "~/components/Child";

export default {
  components: {
    Child,
  },
  // props : 자식 컴포넌트에 데이터를 내려줄 때, 바로 아래 자식에게만 가능, 후손 불가능, 매게체 필요 => provide 사용(매게체 필요x, 반응성은 없음) => vue 패키지에서 computed 가져와서 동작시켜 반응성 유지
};
</script>
