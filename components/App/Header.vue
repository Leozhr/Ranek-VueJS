<template>
  <div>
    <header class="header">
      <nav class="container">
        <NuxtLink to="/"><img src="@/public/img/ranek.svg" alt="Logo"></NuxtLink>
        <NuxtLink to="/" class="login">Login / Vender</NuxtLink>
      </nav>
    </header>
  </div>
</template>

<style scoped>
.header {
  padding: 30px 0px;
  box-shadow: rgba(99, 99, 99, 0.2) 0px 2px 8px 0px;
}

.header nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header nav img {
  transform: scale(3);
}

.header nav .login {
  padding: 15px 40px;
  background: #87f;
  color: white;
  font-size: 1.25rem;
  text-transform: uppercase;
  border-radius: 10px;
}
</style>