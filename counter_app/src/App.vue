<script setup>
import { ref } from 'vue';

// countの初期値
const count = ref(0)

// クリアボタンを押したときにリセットがされる関数
const clear = () => {
  count.value = 0;
}

</script>

<template>
    <h1>カンターアプリ</h1>
    <!-- プラスとマイナスボタン -->
    <div class="button">
        <button @click="count++">+</button>
        <button @click="count--">-</button>
    </div>
    <!-- クリアボタン -->
    <div>
        <button @click="clear">クリア</button>
    </div>
    <!-- カウンター表示 -->
    <div>
        <p>カウンター表示: {{ count }}</p>
    </div>
</template>

<style>
.button {

}

</style>
