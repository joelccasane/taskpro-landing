<template>
    <div class="card">
        <div class="card__header">
            <span>{{ id }}</span>
        </div>
        <h2>{{ title }}</h2>
        <p>{{ description }}</p>
    </div>
</template>

<script setup lang="ts">
defineProps<{
    id: string;
    title: string;
    description: string;
}>();
</script>

<style scoped lang="scss">
.card {
    &__header {
        display: flex;
        justify-content: center;
        align-items: center;
        border-radius: 12px;
        width: 75px;
        height: 75px;
        margin: 0 auto 1rem;
        border: 4px solid $background-light;
        background-color: $primary-color;

        span {
            font-size: 36px;
            font-weight: 800;
            color: $background-light;
        }
    }
    h2 {
        max-width: 200px;
        width: 100%;
        font-size: 18px;
        margin-bottom: 0.6rem;
        text-align: center;
        color: $background-light;
    }
    p {
        max-width: 180px;
        width: 100%;
        margin: auto;
        text-align: center;
        color: $neutral-gray;
    }
}
</style>
