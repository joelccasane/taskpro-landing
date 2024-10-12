<template>
    <section class="hero">
        <div class="hero__container">
            <div class="hero__data">
                <h1>
                    {{ hero.title }}
                </h1>
                <p>
                    {{ hero.description[0] }}
                </p>
                <p>
                    {{ hero.description[1] }}
                </p>
                <HeroButtons></HeroButtons>
            </div>
            <HeroImage></HeroImage>
        </div>
    </section>
</template>

<script setup lang="ts">
import HeroButtons from '@/components/HeroButtons.vue';
import HeroImage from '@/components/HeroImage.vue';
import { hero } from '@/data/data.json';
</script>

<style scoped lang="scss">
.hero {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    padding: 5.5rem 1.5rem;
    background-color: $background-light;

    &__container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        width: 100%;
        max-width: 980px;
    }

    &__data {
        max-width: 600px;
        width: 100%;
        h1 {
            font-size: 3.5rem;
            line-height: 1.1;
            color: $primary-color;
            font-weight: 800;
        }
        p {
            width: 100%;
            max-width: 450px;
            margin: 12px 0px;
            font-size: 20px;
            color: $secondary-color;
        }
    }
}
</style>
