<template>
  <router-link to="/" class="button-more">
    <span></span>Ver mais
    <svg
      width="14"
      height="8"
      viewBox="0 0 14 8"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M1 0.765868L7 6.76587L13 0.765869"
        stroke="#F9154F"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>
  </router-link>
</template>

<style scoped>
.button-more {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  width: 100%;
  max-width: 296px;
  padding: 10px 15px;
  border-radius: 8px;
  border: 1px solid #f9154f;
  color: #f9154f;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  letter-spacing: 0.02rem;
  background-color: transparent;
  text-decoration: none;
}
</style>
