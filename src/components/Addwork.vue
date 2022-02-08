<template>
  <v-container mt-5>
    <h1 class="red text-center">การบ้าน/ งานที่ได้รับหมอบหมาย</h1>
    <h3>เพิ่มงาน</h3>
    <v-select
      v-model="subject"
      :items="items"
      label="--กรุณาเลือกหัวข้อ--"
      solo
    ></v-select>
    <h3>เพิ่มรายการ</h3>
    <v-text-field v-model="work" label="รายการ" outlined></v-text-field>
    <v-btn color="success" class="mr-4" @click="addTodo()">เพิ่ม</v-btn>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      subject: "",
      work: "",
      items: ["วิชา Web", "วิชา SA", "วิชา ML", "อื่นๆ"],
      selectedItem: 1,
      additems: "",
    };
  },
  methods: {
    addTodo() {
      this.additems = this.subject + " " + this.work;
      this.$emit("rtb", this.additems);
    },
  },
};
</script>

<style></style>
