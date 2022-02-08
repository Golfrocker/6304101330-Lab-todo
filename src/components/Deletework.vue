<template>
  <v-container>
    <h1 class="cyan text-center">รายการที่เพิ่ม</h1>
    <div class="d-flex flex-wrap">
      <v-card
        class="pink lighten-5 mx-auto mt-5"
        max-width="344"
        v-for="(item, i) in tt"
        :key="i"
      >
        <v-card-text>
          <p class="text-h4 text--primary">{{ item.text }}</p>
          <div class="text--primary">{{ item.text }}</div>
        </v-card-text>

        <v-card-actions>
          <v-btn
            dark
            color="red"
            @click="deleteTodo(i)"
            v-bind="attrs"
            v-on="on"
          >
            ลบ
          </v-btn>
        </v-card-actions>
      </v-card>
    </div>
  </v-container>
</template>

<script>
export default {
  props: ["tt"],

  data() {
    return {};
  },
  methods: {
    deleteTodo(index) {
      this.tt.splice(index, 1);
    },
  },
};
</script>

<style></style>
