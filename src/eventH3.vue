<!--이벤트핸들링-키 수식어-->
<template>
  <input type="text" @keydown.ctrl.shift.enter="handler" />
</template>

<script>
export default {
  methods: {
    handler() {
      console.log("Enter!!");
    },
  },
};
</script>