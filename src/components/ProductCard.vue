<template>
  <article class="card">
    <header class="card-header">
      <div class="thumbnail">
        <img src="/motos.png" />
      </div>
      <p class="title">Moto</p>
    </header>

    <p class="price">Crédito de <span>R$ 12.000,00</span></p>

    <p class="installment">Parcelas inicial de <span>R$80,14</span></p>

    <div class="text">
      <p>Taxa de administração: 17.00%</p>
      <p>Fundo de reserva: 5.00%</p>
      <p>Prazo do plano: X meses</p>
    </div>

    <router-link to="/checkout" class="button"> Aproveitar Plano </router-link>
  </article>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'ProductCard',
});
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 24px 18px;
  border-radius: 8px;
  box-shadow: 0px 4px 8px 2px #2626261f;
}

.card-header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 8px;
  margin-bottom: 14px;
}
.card-header .title {
  display: block;
  margin: 0px;
  font-weight: 700;
  color: #111111;
  font-size: 28px;
  letter-spacing: 0.04rem;
}
.thumbnail {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 42px;
  height: 38px;
}
.thumbnail img {
  display: flex;
  width: 100%;
  height: 100%;
  object-fit: contain;
}

.price {
  display: block;
  margin: 0px;
  margin-bottom: 14px;
  color: #111111;
  font-size: 24px;
  line-height: 28px;
  font-weight: 400;
}
.price span {
  display: block;
  color: #f9154f;
  font-size: 26px;
  line-height: 30px;
  font-weight: 700;
}

.installment {
  display: block;
  color: #111111;
  font-size: 20px;
  line-height: 24px;
  font-weight: 400;
}
.installment span {
  display: block;
  font-weight: 700;
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

.button {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  padding: 13px;
  border-radius: 4px;
  background-color: #631079;
  color: #ffffff;
  font-size: 14px;
  font-weight: 400;
  letter-spacing: 0.02rem;
  border: none;
  text-decoration: none;
}
</style>
