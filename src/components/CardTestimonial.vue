<template>
    <div class="card">
        <div class="card__container">
            <p>{{ description }}</p>
        </div>
        <div class="card__footer">
            <p class="card__person">{{ person }}</p>
            <span class="card__field">{{ field }}</span>
        </div>
    </div>
</template>

<script setup lang="ts">
defineProps<{
    description: string;
    person: string;
    field: string;
}>();
</script>

<style scoped lang="scss">
.card {
    max-width: 310px;
    color: $primary-color;
    background-color: $background-light;
    overflow: hidden;
    transition:
        transform 0.3s ease,
        box-shadow 0.3s ease;

    &:hover {
        transform: translateY(-2px);
        box-shadow: 0 6px 8px rgba($primary-color, 0.5);
    }

    &__container {
        padding: 1rem;
    }

    &__footer {
        padding: 0.6rem 1rem;
        background-color: $secondary-color;
        color: $background-light;
        p {
            font-weight: bold;
        }

        span {
            font-size: 0.875rem;
        }
    }
}
</style>
