<template>
    <div class="col-4">
        <div class="card p-2 mb-3">
            <p class="text-center">{{ pokemon.name }}</p>
            <img
                class="card-img-top"
                height="80px"
                alt="pokemon_image"
                :src="urlBaseSvg">
        </div>
    </div>
</template>

<script setup>

const pokemon = defineProps(['name', 'urlBaseSvg'])

</script>