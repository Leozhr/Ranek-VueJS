<template>
  <div>
    <div v-for="produto in produtos" :key="produto.id">
      <h2>{{ produto.nome }}</h2>
      <p>{{ produto.descricao }}</p>
      <span>{{ produto.preco }}</span>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import { $axios } from "@/services/axios"
import { iProdutos } from "@/interfaces/iUProdutos"

export default defineComponent({
  setup() {
    const produtos = ref<iProdutos[]>([])

    const fetchApi = async () => {
      await $axios.get<iProdutos[]>('produto')
        .then(response => produtos.value = response.data)
        .catch(error => console.log(error.message))
    }
    onMounted(fetchApi)

    return { produtos }
  }
})
</script>

<style scoped></style>