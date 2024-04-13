<template>
  <header class="header">
    <div class="content">
      <img class="logo" src="/logo.svg" />

      <div class="dash" />
    </div>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  width: 100%;
  padding: 24px 58px;
  background-color: #631079;
}

.header .content {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 16px;
  width: 100%;
}

.header .content .logo {
  display: flex;
  width: 100%;
  max-width: 103px;
}

.header .content .dash {
  display: flex;
  width: 2px;
  height: 32px;
  background-color: #ffffff;
}
</style>
