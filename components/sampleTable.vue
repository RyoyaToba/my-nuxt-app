<template>
  <div class="table-container">
    <table class="custom-table">
      <thead>
        <tr>
          <th v-for="col in columns" :key="col.key">{{ col.label }}</th>
          <th v-if="showDelete">操作</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(row, rowIndex) in data" :key="rowIndex">
          <td v-for="col in columns" :key="col.key">{{ row[col.key] }}</td>
          <td v-if="showDelete">
            <button @click="removeRow(rowIndex)" class="delete-btn">削除</button>
          </td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
defineProps({
  columns: Array,
  data: Array,
  showDelete: { type: Boolean, default: true }
});

const emit = defineEmits(["removeRow"]);

const removeRow = (index) => {
  emit("removeRow", index);
};
</script>

<style scoped>
/* コンテナの余白 */
.table-container {
  overflow-x: auto;
  padding: 16px;
}

/* テーブルの基本デザイン */
.custom-table {
  width: 100%;
  border-collapse: collapse;
  border: 1px solid #ddd;
  box-shadow: 2px 2px 8px rgba(0, 0, 0, 0.1);
  border-radius: 8px;
}

/* ヘッダーのデザイン */
.custom-table thead {
  background-color: #f4f4f4;
  color: #333;
}

.custom-table th, .custom-table td {
  border: 1px solid #ddd;
  padding: 10px;
  text-align: left;
}

/* ホバー時の背景色 */
.custom-table tbody tr:hover {
  background-color: #f9f9f9;
}

/* 削除ボタンのデザイン */
.delete-btn {
  background-color: #e3342f;
  color: white;
  padding: 6px 12px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  transition: background-color 0.2s ease-in-out;
}

.delete-btn:hover {
  background-color: #cc1f1a;
}
</style>
