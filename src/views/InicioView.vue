<script setup>
    import { useBebidasStore } from '../stores/bebidas'
    import Recetas from '../components/Recetas.vue'
    const bebidas = useBebidasStore()
</script>

<template>
    <h1 class="text-6xl font-extrabold text-center">Recetas</h1>

    <p v-if="bebidas.noRecetas" class="my-10 text-center text-2xl">No hay Resultados, empieza a buscar con el Formulario</p>

    <div v-else class="grid grid-cols-1 md:grid-cols-2 2xl:grid-cols-5 my-10 gap-10">
        <Recetas
            v-for="receta in bebidas.recetas"
            :receta="receta"
            :key="receta.idDrink"
        />
    </div>
</template>
