<template>
  <div class="ex01">
    <div>名前：{{ name }}</div>
    <div>年齢：{{ age }}歳</div>
    <div>10年後の年齢：{{ age + 10 }}歳</div>
    <span>趣味：</span>
    <span v-for="hobby of hobbies" v-bind:key="hobby">{{ hobby }} </span>
    <br />
    <a :href="url">自社ページリンク</a>
    <br />
    <img :src="imgUrl" />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Ex01 extends Vue {
  private name = "山田太郎";
  private age = 31;
  private hobbies = ["スイム", "バイク", "ラン"];
  private url = "https://www.rakus-partners.co.jp/";
  private imgUrl = "img/shirotan.jpeg";
}
</script>

<style scoped>
.ex01 {
  text-align: left;
  border: solid;
}
</style>
