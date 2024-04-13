<template>
  <header class="header">
    <div class="content">
      <img class="logo" src="/logo-digital.svg" />
    </div>
  </header>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  width: 100%;
  padding: 4px 25px;
  background-color: #3c1053;
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
  max-width: 125px;
}
</style>
