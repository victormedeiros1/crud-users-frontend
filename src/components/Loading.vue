<script>
export default {
  name: 'Loading'
}
</script>

<template>
  <svg class="loading" viewBox="22 22 44 44">
    <circle
      class="loading__circle"
      stroke="white"
      stroke-width="3.6"
      fill="transparent"
      r="20.2"
      cx="44"
      cy="44"
    />
  </svg>
</template>
<style lang="scss" scoped>
.loading {
  width: 64px;
  height: 64px;

  animation: loading-rotate 1.4s linear infinite;
  -webkit-animation: loading-rotate 1.4s linear infinite;
}

.loading > circle.loading__circle {
  stroke: var(--light);
  stroke-dasharray: 80px, 200px;
  stroke-dashoffset: 0px;

  animation: loading-stroke-circle 1.4s ease-in-out infinite;
  -webkit-animation: loading-stroke-circle 1.4s ease-in-out infinite;

  &:hover {
    stroke: var(--white);
  }
}

@keyframes loading-rotate {
  0% {
    transform: rotate(0deg);
    -webkit-transform: rotate(0deg);
  }

  100% {
    transform: rotate(360deg);
    -webkit-transform: rotate(360deg);
  }
}

@keyframes loading-stroke-circle {
  0% {
    stroke-dasharray: 1px, 200px;
    stroke-dashoffset: 0;
  }

  50% {
    stroke-dasharray: 100px, 200px;
    stroke-dashoffset: -15px;
  }

  100% {
    stroke-dasharray: 100px, 200px;
    stroke-dashoffset: -125px;
  }
}
</style>
