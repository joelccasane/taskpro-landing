<template>
    <div class="hero__links">
        <a href="javascript:void(0)">
            <GPlayBrand />
            <span>Disponible en<span class="bold">Google Play</span></span>
        </a>
        <a href="javascript:void(0)">
            <AppleBrand />
            <span>Descárgalo en la <span class="bold">App Store</span></span>
        </a>
    </div>
</template>

<script setup lang="ts">
import AppleBrand from '@/assets/icons/AppleBrand.vue';
import GPlayBrand from '@/assets/icons/GPlayBrand.vue';
</script>

<style scoped lang="scss">
.hero__links {
    display: flex;
    gap: 1.5rem;
    margin-top: 1rem;
    a {
        display: inline-flex;
        align-items: center;
        min-width: 155px;
        gap: 4px;
        padding: 5px 6px;
        border-radius: 12px;
        text-decoration: none;
        border: 4px solid $neutral-gray;
        color: $background-light;
        background-color: $primary-color;
        transition:
            background-color 0.3s ease,
            box-shadow 0.3s ease,
            border-color 0.3s ease;
        &:hover {
            background-color: $secondary-color;
            box-shadow: 0 6px 8px rgba($primary-color, 0.5);
        }
        span {
            display: inline-flex;
            flex-direction: column;
            font-size: 14px;

            .bold {
                font-weight: 700;
                font-size: 16px;
            }
        }
    }
}
</style>
