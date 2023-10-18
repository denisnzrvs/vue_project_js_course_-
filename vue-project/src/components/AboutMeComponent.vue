<script>
export default {
    name: "HeaderComponent",
    props: ["isLoggedIn"],
    data() {
        return {
            user: {
                name: "Denis",
                surname: "Nazarovs",
                code: "IT21005",
            },
            headerBgColor: "#473d4b",
        };
    },
};
</script>

<template>
    <h1>ABOUT ME</h1>
    <h3>Name: {{ user.name }}</h3>
    <h3>Surname: {{ user.surname }}</h3>
    <h3>Code: {{ user.code }}</h3>
</template>


<style>
template {
    background-color: #282b34;
}

h3 {
    margin-top: 1rem;
    font-family: "Roboto", sans-serif;
    color: white;
}
</style>