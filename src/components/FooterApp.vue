<template>
    <footer class="footer">
        <div class="footer__container">
            <p>
                © {{ dateFooter }} <a href="javascript:void(0)">TaskPro</a>.
                Todos los derechos reservados.
            </p>
            <div class="footer__links">
                <a href="javascript:void(0)" aria-label="Terms and Conditions"
                    >Términos y Condiciones</a
                >
                <a href="javascript:void(0)" aria-label="Privacy Policy"
                    >Política de Privacidad</a
                >
            </div>
        </div>
    </footer>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const dateFooter = ref(new Date().getFullYear().toString());
</script>

<style scoped lang="scss">
.footer {
    background-color: $primary-color;
    padding: 1.8rem 1.5rem;
    &__container {
        display: flex;
        align-items: center;
        justify-content: space-between;
        max-width: 980px;
        margin: 0 auto;
        width: 100%;
        p {
            color: $neutral-gray;
            font-size: 0.875rem;
        }
        a {
            text-decoration: none;
            color: $neutral-gray;
            transition: color 0.3s ease;

            &:hover {
                color: $background-light;
            }
        }
    }
    &__links {
        display: flex;
        gap: 1.3rem;

        a {
            font-size: 0.875rem;
            text-decoration: none;
            color: $neutral-gray;
            transition: color 0.3s ease;

            &:hover {
                color: $background-light;
            }
        }
    }
}
</style>
