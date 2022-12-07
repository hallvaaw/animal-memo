<template>
    <main class="max-w-6xl mx-auto p-6">
        <section class="flex flex-row justify-between">
            <img id="duck" :src="duckImage.image" @click="emitSelection(duckImage.id)" class="rounded w-1/4 h-64 hover:w-1/3 hover:h-72 ease-in duration-150" alt="">
            <img id="dog" :src="dogImage.image" @click="emitSelection(dogImage.id)" class="rounded w-1/4 h-64 hover:w-1/3 hover:h-72 ease-in duration-150" alt="">
            <img id="fox" :src="foxImage.image" @click="emitSelection(foxImage.id)" class="rounded w-1/4 h-64 hover:w-1/3 hover:h-72 ease-in duration-150" alt="">
        </section>
    </main>
</template>

<script>
export default {
    name: 'StartMenu',
    data() {
        return {
            duckImage: {id: 'duck', image: 'https://random-d.uk/api/152.jpg'},
            dogImage: {id: 'dog', image: 'https://random.dog/1800eefa-6a30-48b8-9c3f-ad1eb6fd9abe.jpg'},
            foxImage: {id: 'fox', image: 'https://randomfox.ca/images/90.jpg'}
        }
    },
    emits: ['animal-selection'],
    methods: {
        emitSelection(e) {
            this.$emit('animal-selection', e)
        }
    }
}
</script>
