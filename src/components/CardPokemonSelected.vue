<template>
    <div
        class="card card-pokemon-selected"
        :class="loading
            ?   ''
            :   'animate__animated animate__flipInY'">
        <img
            v-if="pokemon.name"
            class="card-img-top pt-2"
            :src="pokemon.img"
            :alt="pokemon.name">
        <img
            v-else
            class="card-img-top pt-2"
            src="../assets/egg.svg"
            alt="???">
        <div class="card-body">
            <h5 class="card-title text-center">{{ pokemon.name || '???' }} </h5>
            <hr>
            <div class="row">
                <section class="col">
                    <strong>ID: </strong>
                    <span>{{ pokemon.id || '???' }}</span>
                </section>
                <section class="col">
                    <strong>Type: </strong>
                    <span>{{ pokemon.type || '???' }}</span>
                </section>
            </div>
        </div>
    </div>
</template>

<script setup>

import 'animate.css';

const pokemon = defineProps(['name', 'id', 'type', 'img', 'loading'])

</script>

<style scoped>

.card-pokemon-selected {
    height: 75vh;
    background: rgb(240,251,251);
    background: radial-gradient(circle, rgba(240,251,251,1) 0%, rgba(145,216,238,1) 50%, rgba(10,10,10,1) 100%);
    text-align: center;
}
.card-pokemon-selected img {
    height: 250px;
    margin-top: 100px;
}
@media screen and (max-width: 768px) {
    .card-pokemon-selected {
        height: 30vh;
        width: 40%;
        margin: 0 auto 10px auto;
    }
    .card-pokemon-selected img {
        height: 100px;
        margin-top: 45px;
        margin-bottom: 15px;
    }
    .card-body {
        display: none;
    }
}
</style>