<!--vue3-리스트렌더링-->
<template>
  <button @click="handler">Click me!</button>
  <ul>
    <li v-for="{ id, name } in newFruits" :key="id">{{ name }}-{{ id }}</li>
  </ul>
</template>

<script>
import shortid from "shortid";

export default {
  data() {
    return {
      fruits: ["Apple", "Banana", "Cherry"],
      /*
      이러한 형식으로 계산됨
      newFruits: [
        {id: 0, name:'Apple'}
        {id: 1, name:'Banana'}
        {id: 2, name:'Cherry'}
      ]
      */
    };
  },
  computed: {
    newFruits() {
      return this.fruits.map((fruit) => ({
        id: shortid.generate(), //generate() : 간단한 id를 생성
        name: fruit,
      }));
    },
  },
  methods: {
    handler() {
      this.fruits.push("Orange");
    },
  },
};
</script>