<template>
    <div class="socials">
        <div class="text12 gray-text">
            Socials
        </div>
        <div class="socials__items">
            <div
                    class="social-item"
                    v-for="(item, index) in socialsItems" :key="index"
            >
                <div class="social-item__icon">
                    <img :src="$getImageUrl(item.icon)" alt="">
                </div>
                <div class="social-item__content">
                    <div class="social-item__title text12 gray-text">
                        {{item.title}}
                    </div>
                    <div class="social-item__desc text14 gray-dark-text medium-text">
                        <a
                                target="_blank"
                                :href="item.link"
                                class="underline-text"
                        >
                            {{item.desc}}
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Socials",
        data() {
            return {
                socialsItems: [
                    {
                        icon: 'ig.svg',
                        title: 'Instagram',
                        desc: '@marsel__gabbasov',
                        link: 'https://www.instagram.com/marsel__gabbasov/',
                    },
                    {
                        icon: 'github.svg',
                        title: 'Github',
                        desc: '@Gabbasov98',
                        link: 'https://github.com/Gabbasov98',
                    },
                    {
                        icon: 'linkedin.svg',
                        title: 'Linkedin',
                        desc: '@marsel-gabbasov',
                        link: 'https://www.linkedin.com/in/marsel-gabbasov-35a814219/',
                    },
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
    .socials{
        padding: 2em 0;
        border-top: 1px solid $gray-light;
        &__items{
            margin-top: 1.25em;
            @include grid100gap(1.25em);
        }
    }

    .social-item{
        display: flex;
        align-items: center;
        &__icon{
            @include center;
            width: 2em;
            height: 2em;
            border-radius: 50%;
            margin-right: 1em;
            flex-shrink: 0;
            box-shadow: 0px 4.034px 16.135px 0px rgba(0, 0, 0, 0.06);
            img{
                width: 100%;
            }
        }
        &__content{
            @include grid100gap(.25em);
        }
        &__desc{
            word-break: break-word;
        }
    }

</style>
