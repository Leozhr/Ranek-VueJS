<template>
  <div id="app">
    <AppHeader />
    <main id="main">
      <slot />
    </main>
    <AppFooter />
  </div>
</template>

<style>
@import url("@/public/css/default.css");

#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

#main {
  flex: 1;
}
</style>