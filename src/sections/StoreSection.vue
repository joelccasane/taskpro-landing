<template>
    <section class="store">
        <div class="store__container">
            <h2>{{ store.title }}</h2>
            <p>{{ store.description[0] }}</p>
            <p>{{ store.description[1] }}</p>
            <HeroButtons></HeroButtons>
        </div>
    </section>
</template>

<script setup lang="ts">
import { store } from '@/data/data.json';
import HeroButtons from '@/components/HeroButtons.vue';
</script>

<style scoped lang="scss">
.store {
    background-color: $background-light;
    padding: 5rem 1.5rem;
    display: flex;
    justify-content: center;

    &__container {
        width: 100%;
        max-width: 980px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }
    h2 {
        max-width: 700px;
        font-size: 3rem;
        line-height: 1.1;
        font-weight: 800;
        text-align: center;
    }
    p {
        max-width: 600px;
        margin: 12px 0;
        font-size: 20px;
        color: $secondary-color;
        text-align: center;
    }
}
</style>
