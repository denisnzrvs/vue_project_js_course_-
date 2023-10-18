<script>
export default {
    data() {
        return {
            homeActive: true, // Set the HOME button to be active by default
            aboutMeActive: false,
        };
    },
    methods: {
        showHome() {
            this.homeActive = true;
            this.aboutMeActive = false;
            this.$emit("show-home");
        },
        showAboutMe() {
            this.homeActive = false;
            this.aboutMeActive = true;
            this.$emit("show-about-me");
        },
    },
};
</script>


<template>
    <div class="container">
        <button href="#" class="btn" :class="{ active: homeActive }" @click="showHome">HOME</button>
        <button href="#" class="btn" :class="{ active: aboutMeActive }" @click="showAboutMe">ABOUT ME</button>
    </div>
</template>

<style>
.container {
    margin-top: 2rem;
    display: flex;
    flex-direction: column;
    align-items: center;
    background-color: #282b34;
    height: 100%;
    width: 100%;
    color: green;
}

.btn.active {
    background-color: orange;
    color: white;
}

button {
    margin-bottom: 1rem;
    font-family: "Roboto", sans-serif;
    background-color: #473d4b;
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 50px;
    font-weight: bold;
    text-decoration: none;
}
</style>
