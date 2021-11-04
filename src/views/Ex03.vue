<template>
  <div class="ex03">
    <form>
      <div>
        <input type="text" v-model="num1" /> +
        <input type="text" v-model="num2" /> = {{ Number(num1) + Number(num2) }}
      </div>
    </form>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Ex02 extends Vue {
  private num1 = "";
  private num2 = "";
}
</script>

<style></style>
