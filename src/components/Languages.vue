<template>
    <div class="languages">
        <div class="text12 gray-text">
            Languages
        </div>
        <div class="languages__items">
            <div
                    class="language-item"
                    v-for="(item, index) in languagesItems" :key="index"
            >
                <div class="language-item__icon">
                    <img :src="$getImageUrl(item.icon)" alt="">
                </div>
                <div class="language-item__content">
                    <div class="language-item__title text14 gray-dark-text medium-text">
                        {{item.title}}
                    </div>
                    <div class="language-item__desc text12 gray-text">
                        {{item.desc}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Languages",
        data() {
            return {
                languagesItems: [
                    {
                        icon: 'russia.svg',
                        title: 'Russian',
                        desc: 'Native',
                    },
                    {
                        icon: 'britain.svg',
                        title: 'English',
                        desc: 'Professional working',
                    },
                    {
                        icon: 'china.svg',
                        title: 'Chinese',
                        desc: 'Intermediate',
                    },
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
    .languages{
        padding: 2em 0;
        border-top: 1px solid $gray-light;
        &__items{
            margin-top: 1.25em;
            @include grid100gap(1.25em);
        }
    }

    .language-item{
        display: flex;
        align-items: center;
        &__icon{
            @include center;
            width: 2em;
            height: 2em;
            margin-right: 1em;
            flex-shrink: 0;
            img{
                filter: drop-shadow(0px 4.034px 16.135px rgba(0, 0, 0, 0.06));
                width: 100%;
                border-radius: .25em;
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
