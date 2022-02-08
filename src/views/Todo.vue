<template>
  <div>
    <Addwork @rtb="Add"></Addwork>
    <Deletework :tt="n"></Deletework>
  </div>
</template>

<script>
import Addwork from "../components/Addwork.vue";
import Deletework from "../components/Deletework.vue";
export default {
  data() {
    return {
      n: [
        { text: "วิชา Web Assignment500" },
        { text: "วิชา ML Assignment1" },
        { text: "วิชา ML ออกแบบ" },
      ],
    };
  },
  components: { Addwork, Deletework },
  methods: {
    Add(i) {
      this.n.push({ text: i });
    },
  },
};
</script>

<style></style>
