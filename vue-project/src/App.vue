<script setup>
import { ref } from 'vue'
import HeaderComponent from './components/HeaderComponent.vue';
import NavigationComponent from './components/NavigationComponent.vue';
import AboutMeComponent from './components/AboutMeComponent.vue';
import HomeComponent from './components/HomeComponent.vue';
const isLoggedIn = ref(false);
</script>

<script>
export default {
  components: {
    NavigationComponent,
  },
  data() {
    return {
      homeVisible: true, // Set one component to be initially visible
      aboutMeVisible: false,
    };
  },
  methods: {
    showHome() {
      this.homeVisible = true;
      this.aboutMeVisible = false;
    },
    showAboutMe() {
      this.homeVisible = false;
      this.aboutMeVisible = true;
    },
  },
};
</script>

<template>
  <header>
    <HeaderComponent :isLoggedIn="isLoggedIn" @update:isLoggedIn="isLoggedIn = $event">
    </HeaderComponent>
  </header>

  <main>
    <div class="row" v-show="isLoggedIn">
      <div class="col">
        <NavigationComponent @show-home="showHome" @show-about-me="showAboutMe" />
      </div>

      <div class="col">
        <HomeComponent v-if="homeVisible" />
        <AboutMeComponent v-if="aboutMeVisible" />
      </div>
    </div>
  </main>
</template>



<style>
body {
  background-color: #282b34;
  margin: 0px;
}

.row {
  display: flex;
  flex-direction: row;
  flex: 1;
  height: 100vh;
  width: 100%;
}

.col {
  display: flex;
  flex-direction: column;
  flex: 1;
  height: 100vh;
  width: 50%;
  color: green;
}
</style>
