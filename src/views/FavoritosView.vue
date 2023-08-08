<script setup>
    
    import Recetas from '../components/Recetas.vue'
    
    import { useFavoritosStore } from '../stores/favoritos';

    const favoritos = useFavoritosStore()

</script>

<template>

    <h1 class="text-6xl font-extrabold">Favoritos</h1>

    <p v-if="favoritos.noFavoritos" class="my-10 text-center text-2xl">No hay Favoritos</p>

    <div v-else class="grid grid-cols-1 md:grid-cols-2 2xl:grid-cols-5 my-10 gap-10">
        <Recetas
            v-for="receta in favoritos.favoritos"
            :receta="receta"
            :key="receta.idDrink"
        />
    </div>

</template>