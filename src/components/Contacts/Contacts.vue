<template>
    <div class="contacts">
        <div class="contacts__items">
            <div
                    class="contact-item"
                    v-for="(item, index) in contactsItems" :key="index"
            >
                <div class="contact-item__icon">
                    <img :src="$getImageUrl(item.icon)" alt="">
                </div>
                <div class="contact-item__content">
                    <div class="contact-item__title text12 gray-text">
                        {{item.title}}
                    </div>
                    <div class="contact-item__desc text14 gray-dark-text medium-text">
                        <span v-if="item.link === ''">
                            {{item.desc}}
                        </span>
                        <a
                                v-else
                                :href="item.link"
                                :target="item.isUnderline ? '_blank' : ''"
                                :class="{ 'underline-text' : item.isUnderline}"
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
    import './Contacts.scss';
    export default {
        name: "Contacts",
        data() {
            return {
                contactsItems: [
                    {
                        icon: 'mail.svg',
                        title: 'Email',
                        desc: 'marsel1498@gmail.com',
                        link: 'mailto:marsel1498@gmail.com',
                        isUnderline: false
                    },
                    {
                        icon: 'chain.svg',
                        title: 'Website',
                        desc: 'https://github.com/Gabbasov98',
                        link: 'https://github.com/Gabbasov98',
                        isUnderline: true
                    },
                    {
                        icon: 'tg.svg',
                        title: 'Telegram',
                        desc: '@Marsel_Gabbasov',
                        link: 'https://t.me/Marsel_Gabbasov',
                        isUnderline: true
                    },
                ]
            }
        }
    }
</script>

<style scoped>

</style>
