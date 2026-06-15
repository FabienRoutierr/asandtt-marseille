<template>
  <div>
    <AppNavbar />
    <main class="layout-main">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>

<style scoped>
.layout-main {
  padding-top: 120px;
}

@media (max-width: 900px) {
  .layout-main {
    padding-top: 80px;
  }
}
</style>