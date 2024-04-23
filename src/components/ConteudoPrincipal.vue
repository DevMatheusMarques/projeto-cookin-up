<script lang="ts">
import SelecionarIngredientes from "@/components/SelecionarIngredientes.vue";
import Tag from "@/components/Tag.vue";
import SuaLista from "@/components/SuaLista.vue";
import MostrarReceitas from "@/components/MostrarReceitas.vue";
import mostrarReceitas from "@/components/MostrarReceitas.vue";

type Pagina = 'SelecionarIngredientes' | 'MostrarReceitas';
export default {
  computed: {
    mostrarReceitas() {
      return mostrarReceitas
    }
  },
  components: {MostrarReceitas, SuaLista, Tag, SelecionarIngredientes},
  data() {
    return {
      ingredientes: [] as string[],
      conteudo: 'SelecionarIngredientes' as Pagina
    }
  },
  methods: {
    adicionarIngrediente(ingrediente: string) {
      this.ingredientes.push(ingrediente);
    },

    removerIngredientes(ingrediente:string) {
      this.ingredientes = this.ingredientes.filter(iLista => ingrediente !== iLista);
    },

    navegar(pagina: Pagina) {
      this.conteudo= pagina;
    }
  }

}
</script>

<template>
  <main class="conteudo-principal">
    <SuaLista :ingredientes="ingredientes" />

    <KeepAlive include="SelecionarIngredientes">
      <SelecionarIngredientes v-if="conteudo === 'SelecionarIngredientes'"
                              @adicionar-ingrediente="adicionarIngrediente"
                              @remover-ingrediente="removerIngredientes"
                              @buscar-receitas="navegar('MostrarReceitas')"
      />

      <MostrarReceitas v-else-if="conteudo === 'MostrarReceitas'"
                       :ingredientes="ingredientes"
                       @editar-receitas="navegar('SelecionarIngredientes')"
      />
    </KeepAlive>
  </main>
</template>

<style scoped>
.conteudo-principal {
  padding: 6.5rem 7.5rem;
  border-radius: 3.75rem 3.75rem 0rem 0rem;
  background: var(--creme, #FFFAF3);
  color: var(--cinza, #444);

  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 5rem;
}

@media only screen and (max-width: 1300px) {
  .conteudo-principal {
    padding: 5rem 3.75rem;
    gap: 3.5rem;
  }
}

@media only screen and (max-width: 767px) {
  .conteudo-principal {
    padding: 4rem 1.5rem;
    gap: 4rem;
  }
}
</style>