<template>
  <div class="ex02">
    <div>名前：{{ name }}</div>
    <div>年齢：{{ age }}歳</div>
    <div>10年後の年齢：{{ after10age }}歳</div>
    <span>趣味：</span>
    <span v-for="hobby of hobbies" v-bind:key="hobby">{{ hobby }} </span>
    <br />
    <a :href="url">自社ページリンク</a>
    <br />
    <img :src="imgUrl" />
    <button type="button" v-on:click="onclick" v-bind:disabled="canNotClick">
      ボタン
    </button>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";

@Component
export default class Ex02 extends Vue {
  private name = "";
  private age = 0;
  private after10age = 0;
  private hobbies = new Array<string>();
  private url = "";
  private imgUrl = "";
  private canNotClick = false;

  onclick(): void {
    this.name = "山田太郎";
    this.age = 31;
    this.after10age = this.age + 10;
    this.hobbies = ["スイム", "バイク", "ラン"];
    this.url = "https://www.rakus-partners.co.jp/";
    this.imgUrl = "img/shirotan.jpeg";
    this.canNotClick = true;
  }
}
</script>

<style>
.ex02 {
  text-align: left;
  border: solid;
}
</style>
