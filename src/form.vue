<!--폼 입력 바인딩-->
<!--단방향 데이터 바인딩-->
<template>
  <h1>{{ msg }}</h1>
  <input type="text" :value="msg" @input="msg = $event.target.value" />
  <!-- 
  v-model="msg" (한글을 입력할때는 위처럼, 영어는 둘다 상관 없음)
  -->
  <h1>{{ checked }}</h1>
  <input type="checkbox" v-model="checked" />
</template>

<script>
export default {
  data() {
    return {
      msg: "Hello world!",
      checked: false,
    };
  },
  methods: {
    /*
    handler(event) {
      console.log(event.target.value);
      // 반응성을 통해 연결된 부분의 내용도 변경
      this.msg = event.target.value;
    },
    */
  },
};
</script>