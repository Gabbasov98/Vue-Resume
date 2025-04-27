<template>
  <div class="wrapper">
    <aside class="sidebar">
      <teleport v-if="currentTarget" :to="currentTarget">
        <About/>
      </teleport>
      <div ref="desktopTarget" />
      <Contacts/>
      <Socials/>
      <Languages/>
      <Interests/>
    </aside>
    <main class="main">
      <div ref="mobileTarget" />
      <Education/>
      <Achievements/>
      <Skills/>
      <Projects/>
    </main>
  </div>
</template>

<script>
  import About from "#/components/About.vue";
  import Contacts from "#/components/Contacts.vue";
  import Socials from "#/components/Socials.vue";
  import Languages from "#/components/Languages.vue";
  import Interests from "#/components/Interests.vue";
  import Education from "#/components/Education.vue";
  import Skills from "#/components/Skills.vue";
  import Achievements from "#/components/Achievements.vue";
  import Projects from "#/components/Projects.vue";
  export default {
    components: {
      About,
      Contacts,
      Socials,
      Languages,
      Interests,
      Education,
      Skills,
      Achievements,
      Projects
    },
    data() {
      return {
        currentTarget: null
      }
    },
    mounted() {
      this.updateTarget()
      window.addEventListener('resize', this.updateTarget)
    },
    beforeUnmount() {
      window.removeEventListener('resize', this.updateTarget)
    },
    methods: {
      updateTarget() {
        const isMobile = window.innerWidth <= 992
        this.currentTarget = isMobile
                ? this.$refs.mobileTarget
                : this.$refs.desktopTarget
      }
    }
  }
</script>

<style scoped>

</style>
