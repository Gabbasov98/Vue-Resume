<template>
    <div class="interests">
        <div class="text12 gray-text">
            Hobbies & Interests
        </div>
        <div class="interests__items">
            <div
                    class="interest-item"
                    v-for="(item, index) in interestsItems" :key="index"
            >
                <div class="interest-item__icon">
                    <img :src="$getImageUrl(item.icon)" alt="">
                </div>
                <div class="interest-item__content">
                    <div class="interest-item__title text14 gray-dark-text medium-text">
                        {{item.title}}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Interests",
        data() {
            return {
                interestsItems: [
                    {
                        icon: 'book.svg',
                        title: 'Books',
                    },
                    {
                        icon: 'Travelling.svg',
                        title: 'Travelling',
                    },
                ]
            }
        }
    }
</script>

<style scoped lang="scss">
    .interests{
        padding: 2em 0 0;
        border-top: 1px solid $gray-light;
        &__items{
            margin-top: 1em;
            @include grid100gap(1em);
        }
    }

    .interest-item{
        display: flex;
        align-items: center;
        &__icon{
            @include center;
            width: 2.1875em;
            height: 2.1875em;
            margin-right: 1em;
            flex-shrink: 0;
            img{
                width: 100%;
            }
        }
        &__content{
            @include grid100gap(.25em);
        }
    }

</style>
