<template>
  <Header />

  <section class="home">
    <h1 class="title">O que você deseja conquistar?</h1>

    <Navigation :categories="categories" />

    <div class="content">
      <p class="warning">Exibindo 8 produtos de 10 totais.</p>

      <div class="products">
        <template v-if="categoryActived === 'automoveis'">
          <ProductCard
            v-for="automovel in automoveis?.products"
            :key="automovel.id"
          />
        </template>

        <template v-if="categoryActived === 'motocicletas'">
          <ProductCard
            v-for="motocicleta in motocicletas?.products"
            :key="motocicleta.id"
          />
        </template>

        <template v-if="categoryActived === 'caminhoes-onibus'">
          <ProductCard
            v-for="caminhao in caminhoesOnibus?.products"
            :key="caminhao.id"
          />
        </template>

        <template v-if="categoryActived === 'imoveis'">
          <ProductCard v-for="imovel in imoveis?.products" :key="imovel.id" />
        </template>
      </div>

      <div class="button-container">
        <ButtonMore />
      </div>
    </div>
  </section>
</template>

<script lang="ts" setup>
import { computed, onMounted, ref } from 'vue';
import Header from '../components/Header/default.vue';
import Navigation from '../components/Home/Navigation.vue';
import ProductCard from '../components/ProductCard.vue';
import ButtonMore from '../components/Home/ButtonMore.vue';
import axios from 'axios';
import { useRoute } from 'vue-router';

const route = useRoute();
const categories = ref<any>([]);

const automoveis = computed(
  () => categories.value.filter((category: any) => category.id === 101)[0]
);

const motocicletas = computed(
  () => categories.value.filter((category: any) => category.id === 102)[0]
);

const caminhoesOnibus = computed(
  () => categories.value.filter((category: any) => category.id === 103)[0]
);

const imoveis = computed(
  () => categories.value.filter((category: any) => category.id === 104)[0]
);

const categoryActived = computed(() => route.params.category);

onMounted(() => {
  axios
    .get('https://orbbits.com.br/servico_mercado_secundario/testFront')
    .then(({ data }) => (categories.value = data.data));
});
</script>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  width: 100%;
  padding: 70px 0px;
}

.home .title {
  display: block;
  font-size: 32px;
  font-weight: 600;
  line-height: 40px;
  text-align: center;
  letter-spacing: 0.01rem;
  margin-bottom: 70px;
}

.content {
  display: flex;
  flex-direction: column;
  width: 100%;
  max-width: var(--max-container);
  margin: 0 auto;
  margin-top: 37px;
}

.warning {
  display: block;
  color: #6f6f6f;
  font-size: 14px;
  font-weight: 600;
  line-height: 22px;
  letter-spacing: 0.01rem;
}

.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 38px 49px;
}

.button-container {
  display: flex;
  width: 100%;
  align-items: center;
  justify-content: center;
  margin-top: 105px;
}
</style>
