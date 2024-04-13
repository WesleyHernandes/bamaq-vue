<template>
  <nav class="navigation">
    <div class="content">
      <router-link
        v-for="category in categories"
        :key="category.id"
        class="option"
        :class="[{ active: categoryActived === getSlug(category.id) }]"
        :to="getSlug(category.id)"
        @click="() => handleClick(getSlug(category.id))"
      >
        {{ category.name }}
      </router-link>
    </div>
  </nav>
</template>

<script lang="ts" setup>
import { useRoute } from 'vue-router';
import { categories_slug } from '../../utils/config';
import { computed } from 'vue';
const route = useRoute();

const categoryActived = computed(() => route.params.category);

defineProps({
  categories: [] as any,
});

const emit = defineEmits(['setSlug']);
const handleClick = (slug: string) => {
  emit('setSlug', slug);
};

const getSlug = (categoryId: number) => {
  return (
    categories_slug.filter((item: any) => item.category_id === categoryId)[0]
      ?.slug || '/'
  );
};
</script>

<style scoped>
.navigation {
  display: flex;
  flex-direction: column;
  width: 100%;
  border-bottom: 4px solid #d9d9d9;
}

.navigation .content {
  display: flex;
  align-items: stretch;
  width: 100%;
  margin: 0 auto;
  max-width: var(--max-container);
  justify-content: space-between;
}

.navigation .content .option {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-grow: 1;
  padding: 16px;
  padding-top: 0px;
  margin-bottom: -4px;
  border: none;
  border-bottom: 4px solid transparent;
  text-decoration: none;
  color: #6f6f6f;
  font-size: 16px;
  line-height: 22px;
  letter-spacing: 0.02rem;
  background-color: transparent;
  text-decoration: none;
}

.navigation .content .option.active {
  color: #631079;
  border-color: #631079;
}
</style>
