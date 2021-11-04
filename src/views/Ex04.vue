<template>
  <div class="ex04">
    <form>
      <div><input type="text" v-model.number="amount1" /></div>
      <div><input type="text" v-model.number="amount2" /></div>
      <div><input type="text" v-model.number="amount3" /></div>
      <div>税抜き価格：{{ subTotal.toLocaleString() }}円</div>
      <div>税込み価格：{{ total.toLocaleString() }}円</div>
    </form>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Ex02 extends Vue {
  private amount1 = 0;
  private amount2 = 0;
  private amount3 = 0;

  get subTotal() {
    return Math.floor(this.amount1 + this.amount2 + this.amount3);
  }

  get total() {
    const tax = 1.1;
    return Math.floor(this.subTotal * tax);
  }
}
</script>

<style></style>
