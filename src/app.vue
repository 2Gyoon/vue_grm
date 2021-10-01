<template>
  <h1>{{ msg }}</h1>
  <input type="text" v-model.trim="msg" />
  <!-- 
    :value="msg" @change="msg = $event.target.value"  
    / v-model.lazy : blur 처리 되어야만 갱신
    / v-model.number : 숫자로 계속 유지해야 할 때 사용
    -->
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello world!",
    };
  },
  watch: {
    msg() {
      console.log(this.msg);
      // trim() : 앞 뒤의 공백 없애줌
    },
  },
};
</script>