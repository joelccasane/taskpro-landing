<template>
    <header class="header">
        <div class="header__container">
            <a href="/">TaskPro</a>
        </div>
    </header>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.header {
    background-color: $primary-color;
    &__container {
        max-width: 980px;
        margin: auto;
        display: flex;
        justify-content: center;
        padding: 0.4rem 1.5rem;
    }
    a {
        font-size: 2rem;
        font-weight: 700;
        color: $background-light;
        text-decoration: none;
    }
}
</style>
