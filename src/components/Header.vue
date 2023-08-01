<script setup>
    import { RouterLink } from 'vue-router'
</script>

<template>
    <header class="bg-slate-800">
        <div class="mx:auto container px-5 py-16">
            <div class="flex justify-between items-center">
                <div>
                    <RouterLink
                        :to="{name: 'inicio'}"
                    >
                        <img class="w-32" src="../../public/img/logo.svg" alt="Logotipo">
                    </RouterLink>
                </div>

                <nav class="flex gap-4">
                    <RouterLink
                        :to="{name: 'inicio'}"
                        class="text-white uppercase font-bold"
                        active-class="text-orange-500"
                    >
                        Inicio
                    </RouterLink>
                    <RouterLink
                        :to="{name: 'favoritos'}"
                        class="text-white uppercase font-bold"
                        active-class="text-orange-500"
                    >
                        Favoritos
                    </RouterLink>
                </nav>
            </div>

            <form 
                class="md:w-1/2 2xl:w-1/3 bg-orange-400 my-32 p-10 rounded-lg shadow space-y-6"
            >
                <div class="space-y-4">
                    <label 
                        for="ingrediente"
                        class="block text-white uppercase font-extrabold text-lg"
                    >
                        Nombre o Ingredientes
                    </label>
                    <input 
                        id="ingrediente"
                        type="text"
                        class="p-3 w-full rounded-lg focus:outline-none"
                        placeholder="Nombre o Ingrediente: ej. Vodka, Tequila, etc"
                    >
                </div>
                <div class="space-y-4">
                    <label 
                        for="categoria"
                        class="block text-white uppercase font-extrabold text-lg"
                    >
                        Categoría
                    </label>
                    <select 
                        id="categoria"
                        class="p-3 w-full rounded-lg focus:outline-none"
                    >
                        <option value="">-- Seleccione --</option>
                    </select>
                </div>

                <input 
                    type="submit"
                    class="bg-orange-800 hover:bg-orange-900 cursor-pointer text-white font-extrabold w-full p-2 rounded-lg uppercase"
                    value="Buscar Recetas"
                >
            </form>
        </div>
    </header>
</template>