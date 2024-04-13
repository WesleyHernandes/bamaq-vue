<template>
  <router-link to="/" class="back">
    <svg
      width="25"
      height="25"
      viewBox="0 0 25 25"
      fill="none"
      xmlns="http://www.w3.org/2000/svg"
    >
      <path
        d="M19.5312 12.7734H5.53125"
        stroke="#3C1053"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
      <path
        d="M12.5312 19.7734L5.53125 12.7734L12.5312 5.77344"
        stroke="#3C1053"
        stroke-width="2"
        stroke-linecap="round"
        stroke-linejoin="round"
      />
    </svg>
    <span>Voltar</span>
  </router-link>
</template>

<style scoped>
.back {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 10px;
  background-color: transparent;
  border: none;
  text-decoration: none;
}
span {
  display: block;
  margin: 0px;
  color: #3c1053;
  font-size: 14px;
  line-height: 17px;
  font-weight: 500;
}
</style>
