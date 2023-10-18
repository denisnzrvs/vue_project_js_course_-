<template>
    <header class="header">
        <h1>KRAKEN.FM</h1>
        <ul>
            <li><a href="#">Login</a></li>
        </ul>
    </header>
</template>

<script>
export default {
    name: "HeaderComponent",
};
</script>


<style scoped>
header {
    background-color: #473d4b;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem;
    width: 100%;
    /* Set the width to 100% to make it span the entire page */
}

.logo {
    font-size: 24px;
    font-weight: bold;
    color: white;
    /* Adjust the color to match your design */
}

/* Style for the button or other element on the right */
.button {
    background-color: #f1f1f1;
    /* Adjust the background color */
    color: #473d4b;
    /* Adjust the text color */
    padding: 10px 20px;
    /* Adjust padding as needed */
    border: none;
    border-radius: 4px;
    font-weight: bold;
    text-decoration: none;
}

h1 {
    all: none;
    color: white;
}
</style>