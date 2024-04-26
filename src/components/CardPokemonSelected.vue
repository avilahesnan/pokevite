<template>
    <div
        class="card card-pokemon-selected"
        :class="loading
            ?   ''
            :   'animate__animated animate__flipInY'">
        <img
            v-if="pokemon.name"
            class="card-img-top pt-2"
            height="350px"
            :src="pokemon.img"
            :alt="pokemon.name">
        <img
            v-else
            class="card-img-top pt-2"
            height="350px"
            src="../assets/egg.svg"
            alt="???">
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }} </h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>XP:</strong>
                    <span>{{ pokemon.xp || '???' }}</span>
                </section>
                <section class="col">
                    <strong>Altura:</strong>
                    <span>{{ pokemon.height || '???' }}</span>
                </section>
            </div>
        </div>
    </div>
</template>

<script setup>

import 'animate.css';

const pokemon = defineProps(['name', 'xp', 'height', 'img', 'loading'])

</script>

<style scoped>

.card-pokemon-selected {
    height: 75vh;
    background: rgb(240,251,251);
    background: radial-gradient(circle, rgba(240,251,251,1) 0%, rgba(145,216,238,1) 50%, rgba(10,10,10,1) 100%);
}

</style>