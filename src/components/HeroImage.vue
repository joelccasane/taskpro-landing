<template>
    <div class="hero__image">
        <picture>
            <img
                src="@/assets/images/phone-one.png"
                alt="Image Iphone 15 Pro Max"
                class="first-phone"
            />
            <img
                src="@/assets/images/phone-two.png"
                alt="Image Samsung S24"
                class="second-phone"
            />
            <img
                src="@/assets/images/phone-three.png"
                alt="Image Google Pixel"
                class="third-phone"
            />
        </picture>
    </div>
</template>

<script setup lang="ts"></script>

<style scoped lang="scss">
.hero__image {
    position: relative;
    max-width: 230px;
    width: 100%;

    .first-phone {
        position: relative;
        top: 12px;
        left: -90px;
        z-index: 18;
    }
    .second-phone {
        position: absolute;
        max-width: 190px;
        top: 30px;
        left: -185px;
        z-index: 0;
        transform: rotate(-8deg);
    }
    .third-phone {
        position: absolute;
        max-width: 160px;
        top: 45px;
        left: 70px;
        z-index: 0;
        transform: rotate(8deg);
    }
}
@media (max-width: 767px) {
    .hero__image {
        display: none;
    }
}

@media (max-width: 1280px) and (min-width: 768px) {
    .hero__image {
        .first-phone {
            position: relative;
            top: 0;
            left: 0;
            z-index: 18;
        }
        .second-phone {
            display: none;
        }
        .third-phone {
            display: none;
        }
    }
}
</style>
