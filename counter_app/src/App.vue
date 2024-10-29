<template>
    <h1>カウンターアプリ</h1>
    <!-- カウンター表示 -->
    <div class="counter-display">
      <p>カウンター表示: [ {{ count }} ]</p>
    </div>
    <!-- プラスとマイナスボタン -->
    <div class="button-group">
        <button @click="count++">+</button>
        <button @click="count--">-</button>
    </div>
    <!-- クリアボタン -->
    <div class="clear-button">
        <button @click="clear">クリア</button>
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

// countの初期値
const count = ref<number>(0) // number型のリアクティブ変数であることの明示

// クリアボタンを押したときにリセットがされる関数
const clear = (): void => { // voidでなにもか返さないことの保証をする
  count.value = 0;
}

</script>

<style scoped>
/* タイトル */
h1 {
  text-align: center;
  font-size: 2rem;
  margin-bottom: 1rem;
}

/* ＋,-ボタン */
.button-group {
  display: flex;
  justify-content: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

/* クリアボタン */
.clear-button {
  display: flex;
  justify-content: center;
  margin-bottom: 1rem;
}

/* カウンター表示 */
.counter-display {
  text-align: center;
  font-size: 1rem;
  margin-top: 1rem;
}

</style>
