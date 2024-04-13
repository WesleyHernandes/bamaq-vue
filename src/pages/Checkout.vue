<template>
  <div class="checkout">
    <Header />
    <Navigation />

    <div class="container">
      <div class="sidebar">
        <p class="subtitle">Bem selecionado</p>
        <p class="title">Carro</p>

        <div class="icon-container">
          <Icon />
        </div>

        <div class="dash" />

        <div class="price">
          <div class="item">
            <p>Crédito</p>
            <span>R$15.000,00</span>
          </div>

          <div class="item">
            <p>Valor da primeira parcela:</p>
            <span>R$126,90</span>
          </div>
        </div>

        <div class="text">
          <p>Taxa de administração: 17.00%</p>
          <p>Fundo de reserva: 5.00%</p>
          <p>Prazo do plano: X meses</p>
        </div>
      </div>

      <div class="content"></div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Header from '../components/Header/digital.vue';
import Navigation from '../components/Checkout/Navigation.vue';
import Icon from '../components/Checkout/Icon.vue';

defineOptions({
  name: 'Checkout',
});
</script>

<style scoped>
.checkout {
  display: flex;
  flex-direction: column;
  width: 100%;
  min-height: 100vh;
  background-color: #f8f8f8;
}
.container {
  display: flex;
  align-items: stretch;
  justify-content: space-between;
  width: 100%;
  max-width: 872px;
  margin: 0 auto;
  gap: 23px;
  padding-top: 25px;
}

.sidebar {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 22px 25px;
  max-width: 263px;
  background-color: #ffffff;
  box-shadow: 0px 1px 6px 0px #1b002833;
}

.subtitle {
  display: block;
  width: 100%;
  margin: 0px;
  margin-bottom: 7px;
  color: #212429;
  font-size: 12px;
  line-height: 24px;
  font-weight: 400;
  text-align: center;
}

.title {
  display: block;
  width: 100%;
  margin: 0px;
  margin-bottom: 16px;
  color: #212429;
  font-size: 18px;
  line-height: 27px;
  font-weight: 700;
  text-align: center;
}

.icon-container {
  display: flex;
  width: 100%;
  margin-bottom: 28px;
  justify-content: center;
}

.dash {
  display: flex;
  width: 100%;
  height: 1px;
  margin-bottom: 24px;
  background-color: #c2c2c2;
}

.price {
  display: flex;
  flex-direction: column;
  gap: 6px;
  margin-bottom: 33px;
}
.price .item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 5px;
}
.price .item p {
  display: block;
  margin: 0px;
  color: #f80c54;
  font-size: 10px;
  line-height: 12px;
  letter-spacing: 0.08rem;
  font-weight: 400px;
  max-width: 110px;
}
.price .item span {
  display: block;
  margin: 0px;
  color: #f80c54;
  font-size: 14px;
  line-height: 21px;
  letter-spacing: 0.08rem;
  font-weight: 600px;
}

.text {
  display: flex;
  flex-direction: column;
  margin-bottom: 14px;
  gap: 2px;
}
.text p {
  display: block;
  margin: 0px;
  color: #6f6f6f;
  font-weight: 400;
  font-size: 12px;
  line-height: 14px;
}

.content {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  min-height: 595px;
  background-color: #ffffff;
}
</style>
