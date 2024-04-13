<template>
  <section class="navigation">
    <div class="button-container">
      <BackButton />
    </div>

    <nav class="navigate">
      <button class="button-nav active">
        <div class="step">1</div>
        <p class="text">Detalhes</p>
      </button>

      <div class="dash" />

      <button class="button-nav">
        <div class="step">2</div>
        <p class="text">Dados</p>
      </button>

      <div class="dash" />

      <button class="button-nav">
        <div class="step">3</div>
        <p class="text">Contrato</p>
      </button>
    </nav>
  </section>
</template>

<script lang="ts" setup>
import BackButton from './BackButton.vue';
</script>

<style scoped>
.navigation {
  position: relative;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  width: 100%;
  padding: 17px;
  background-color: #ffffff;
  border-bottom: 1px solid #e9e9e9;
}
.button-container {
  position: absolute;
  z-index: 10;
  top: 50%;
  left: 25px;
  transform: translateY(-50%);
}
.navigate {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  width: 100%;
  max-width: 322px;
  margin-bottom: 10px;
}
.button-nav {
  position: relative;
  display: flex;
  flex-direction: column;
  background-color: transparent;
  border: none;
  padding-bottom: 5px;
}
.step {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 23px;
  height: 23px;
  background-color: #c2c2c2;
  color: #ffffff;
  font-size: 12px;
  line-height: 18px;
  font-weight: 700;
  border-radius: 100%;
}
.text {
  position: absolute;
  display: block;
  color: #c2c2c2;
  font-size: 10px;
  line-height: 15px;
  white-space: nowrap;
  text-align: center;
  top: 100%;
  left: 50%;
  transform: translateX(-50%);
}
.dash {
  display: flex;
  height: 2px;
  flex-grow: 1;
  margin-top: 12px;
  background-color: #ced3de;
}

.button-nav.active .step {
  background-color: #f80c54;
}
.button-nav.active .text {
  color: #f80c54;
}
</style>
