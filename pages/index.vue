<template>
  <div>
    <h1 class="titulo">👍 Compra ou Venda 👎</h1>
    <ProdutosBuscar />
    <ProdutosLista />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue"

export default defineComponent({
  setup() {


    return {}
  }
})
</script>

<style scoped>
.titulo {
  color: #87f;
  padding: 70px 0px;
  text-align: center;
  font-size: 2.5rem;
}
</style>