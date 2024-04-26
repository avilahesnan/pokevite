<template>
    <div class="col-4 col-md-6 col-xl-3">
        <div class="card p-2 mb-3 card-list-pokemon">
            <p class="text-center">{{ pokemon.name }}</p>
            <img
                class="card-img-top"
                :alt="pokemon.name"
                :src="urlBaseSvg">
        </div>
    </div>
</template>

<script setup>

const pokemon = defineProps(['name', 'urlBaseSvg'])

</script>

<style scoped>

.card-list-pokemon {
    background: rgb(240,251,251);
    background: radial-gradient(circle, rgba(240,251,251,1) 0%, rgba(69,139,135,1) 50%, rgba(10,10,10,1) 100%);
    cursor: pointer;
}
.card-list-pokemon:hover {
    background: radial-gradient(circle, rgba(240,251,251,1) 0%, rgba(106,213,206,1) 50%, rgba(10,10,10,1) 100%);   
}
.card-list-pokemon img {
    height: 80px;
}
.card-list-pokemon img:hover {
    padding: .1rem;
}

</style>