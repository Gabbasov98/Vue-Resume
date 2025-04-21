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
    import './Languages.scss';
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

<style scoped>

</style>
