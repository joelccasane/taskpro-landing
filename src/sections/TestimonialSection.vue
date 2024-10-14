<template>
    <section class="testimonials">
        <h2>TESTIMONIOS</h2>
        <div class="testimonials__container">
            <CardTestimonial
                v-for="tes in testimonials"
                :key="tes.description"
                :description="tes.description"
                :field="tes.field"
                :person="tes.person"
            ></CardTestimonial>
        </div>
    </section>
</template>

<script setup lang="ts">
import CardTestimonial from '@/components/CardTestimonial.vue';
import { testimonials } from '@/data/data.json';
</script>

<style scoped lang="scss">
.testimonials {
    padding: 4rem 1.5rem;
    background-color: $neutral-gray;
    h2 {
        color: $primary-color;
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
        gap: 1.5rem;
        max-width: 980px;
        width: 100%;
        margin: auto;
    }
}
</style>
