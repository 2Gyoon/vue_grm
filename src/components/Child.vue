<!--컴포넌트 provide, inject with components5-->
<template>
  <div>Child: {{ msg.value }}</div>
</template>

<script>
export default {
  inject: ["msg"],
};
</script>

