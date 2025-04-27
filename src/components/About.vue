<template>
    <div class="about">
        <div class="about__img">
            <img src="../assets/img/avatar.jpg" alt="">
        </div>
        <div class="about__name h1">
            Marsel Gabbasov
        </div>
        <div class="about__desc">
            A well-organized, creative and goaloriented graduate possessing excellent communication, problem-solving and leadership skills with a flair to explore Web Development
        </div>
    </div>
</template>

<script>
    export default {
        name: "About"
    }
</script>

<style lang="scss">
    .about{
        &__img{
            width: 6em;
            height: 6em;
            margin-bottom: 1em;
            img{
                width: 100%;
                height: 100%;
                display: block;
                object-fit: cover;
                border-radius: 50%;
            }
        }
        &__desc{
            color: $gray-dark;
            margin-top: 1.8em;
            font-size: 1.125em;
            line-height: 133%;
            font-family: $font2;
        }
    }

</style>
