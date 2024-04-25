<template>
    <main>
        <div class="container">
            <div class="col-sm-12 col-md-6">
                <div class="card">
                    <div class="card-body row">
                        <ListPokemons
                            v-for="pokemon in pokemons"
                            :key="pokemon.name"
                            :name="pokemon.name"
                            :urlBaseSvg="urlBaseSvg + pokemon.url.split('/')[6] + '.svg'" />
                    </div>
                </div>
            </div>
        </div>
    </main>
</template>

<script setup>

import { onMounted, reactive, ref} from 'vue'

import ListPokemons from '../components/ListPokemons.vue'

let urlBaseSvg = ref("https://raw.githubusercontent.com/PokeAPI/sprites/master/sprites/pokemon/other/dream-world/")
let pokemons = reactive(ref())

onMounted(() => {
    fetch('https://pokeapi.co/api/v2/pokemon?limit=494&offset=0')
        .then(res => res.json())
        .then(res => pokemons.value = res.results)
})

</script>