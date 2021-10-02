<!--컴포넌트 emit with components3-->
<template>
  <div class="btn">
    <slot></slot>
  </div>
  <h1 @dblclick="$emit('2gyoon', $event)">ABC</h1>
  <input type="text" v-model="msg" />
</template>

<script>
export default {
  // inheritAttrs: false,
  emits: ["2gyoon", "changeMsg"],
  data() {
    return {
      msg: "",
    };
  },
  watch: {
    msg() {
      this.$emit("changeMsg", this.msg);
    },
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