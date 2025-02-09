<template>
    <header class="header">
      <div class="logo">家計簿アプリ</div>
      <nav class="nav">
        <RouterLink to="/" class="nav-item">ホーム</RouterLink>
        <RouterLink to="/register" class="nav-item">登録</RouterLink>
        <RouterLink to="/category" class="nav-item">カテゴリ</RouterLink>
        <RouterLink to="/dashboard" class="nav-item">ダッシュボード</RouterLink>
      </nav>
      <div class="menu">
        <RouterLink to="/logout" class="menu-item">ログアウト</RouterLink>
      </div>
    </header>
  </template>
  
  <script setup>
  import { RouterLink } from 'vue-router';
  </script>
  
  <style scoped>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 20px;
    background-color: #2cc6b5;
    color: white;
    font-weight: bold;
  }
  
  .logo {
    font-size: 1.5rem;
  }
  
  .nav {
    display: flex;
    gap: 20px;
  }
  
  .nav-item, .menu-item {
    text-decoration: none;
    color: white;
    font-size: 1rem;
    transition: opacity 0.3s;
  }
  
  .nav-item:hover, .menu-item:hover {
    opacity: 0.7;
  }
  </style>
  