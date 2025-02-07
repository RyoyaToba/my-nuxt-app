<template>
    <div>
        <h1>家計簿アプリ</h1>
    </div>
    <sampleTable :columns="columns" :data="data"></sampleTable>
</template>

<script setup>
import sampleTable from '~/components/sampleTable.vue'

// カラム定義
const columns = ref([
  { key: "name", label: "名称" },
  { key: "price", label: "値段" },
  { key: "category", label: "カテゴリ" }
]);

// テーブルデータ
const data = ref([
  { name: "家賃", price: "100000", category: "家賃" },
  { name: "電気代", price: "100000", category: "光熱費" },
  { name: "水道代", price: "10000", category: "光熱費" },
  { name: "ガス代", price: "10000", category: "光熱費" }
]);
</script>

<style>
    /* スタイルの追加例 */
h1 {
  color: #42b883;
  font-family: Arial, sans-serif;
  text-align: center;
}
p {
  text-align: center;
  color: #35495e;
}
</style>