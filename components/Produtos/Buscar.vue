<template>
  <div>
    <form action="">
      <input name="buscar" type="text" id="buscar" v-model="buscar" @keydown.enter.prevent="Procurar()">
    </form>
    {{ buscar }}
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue"
import { Router } from "vue-router"

export default defineComponent({
  setup() {
    const buscar = ref("")
    const $router: Router = useRouter()

    function Procurar(): void {
      $router.push({ query: { q: buscar.value } })
    }

    return { buscar, Procurar }
  }
})
</script>

<style scoped></style>