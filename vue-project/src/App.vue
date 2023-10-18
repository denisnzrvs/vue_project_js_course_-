<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import NavigationComponent from './components/NavigationComponent.vue';
import AboutMeComponent from './components/AboutMeComponent.vue';
import HomeComponent from './components/HomeComponent.vue';
</script>

<template>
  <header>
    <HeaderComponent>

    </HeaderComponent>
  </header>

  <main>
    <div class="row">
      <div class="col">
        <NavigationComponent />
      </div>

      <div class="col">
        <!-- nothing for now! -->
      </div>
    </div>
  </main>
</template>

<style>
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
