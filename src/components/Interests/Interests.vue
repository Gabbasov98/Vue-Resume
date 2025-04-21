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
    import './Interests.scss';
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

<style scoped>

</style>
