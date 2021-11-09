<template>
  <div class="layout_default">
    <NavLeft />
    <div class="wrapper py-3 text-white min-h-screen mr-12">
      <Nuxt />
    </div>
  </div>
</template>

<style>
html {
  font-family: 'Barlow', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

body {
  background-color: #252836;
}

.wrapper {
  margin-left: 142px;
}
</style>
