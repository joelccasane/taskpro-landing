<template>
    <section class="benefits">
        <h2>BENEFICIOS</h2>
        <div class="benefits__container">
            <CardApp
                v-for="ben in benefits"
                :id="ben.id"
                :key="ben.title"
                :title="ben.title"
                :description="ben.description"
            />
        </div>
    </section>
</template>

<script setup lang="ts">
import CardApp from '@/components/CardBenefit.vue';
import { benefits } from '@/data/data.json';
</script>

<style scoped lang="scss">
.benefits {
    padding: 4rem 1.5rem;
    background-color: $secondary-color;
    h2 {
        color: $background-light;
        text-decoration: underline;
        text-underline-offset: 6px;
        text-align: center;
        margin-bottom: 2.5rem;
        font-size: 2.5rem;
    }
    &__container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 2rem;
        max-width: 980px;
        margin: auto;
        width: 100%;
    }
}
</style>
