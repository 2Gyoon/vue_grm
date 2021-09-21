<!--vue3-computed-->
<!--
<template>
  <Fruits />
</template>

<script>
import Fruits from "~/components/Fruits";
export default {
  components: {
    Fruits,
  },
};
</script>
-->

<template>
  <button @click="add">ADD</button>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
  <h1>{{ reversedMessage }}</h1>
</template>

<script>
export default {
  data() {
    return {
      // Getter, Setter
      msg: "Hello Computed!",
    };
  },
  computed: {
    // 읽기 전용 Getter
    // 계산된 데이터
    // 캐싱 : 한 번 연산 해둔 값이 있으면 저장해둔 값을 사용함, 최적화 목적
    /*
    reversedMessage() {
      return this.msg.split("").reverse().join("");
    },
    */
    // Getter, Setter
    reversedMessage: {
      get() {
        return this.msg.split("").reverse().join("");
      },
      set(newValue) {
        this.msg = newValue;
      },
    },
  },
  methods: {
    /*
    reverseMessage() {
      return this.msg.split("").reverse().join("");
    },
    */
    add() {
      this.reversedMessage += "!?";
      // this.msg += "!?";
    },
  },
};
</script>