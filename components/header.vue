<template>
    <nav>
        <nuxt-link to="/">Home</nuxt-link>
        <nuxt-link to="/recipes">Recipes</nuxt-link>
        <nuxt-link to="/contact">Contact</nuxt-link>
    </nav>
</template>

<style>
nav {
    background: blue;
    margin-top: 0;
    padding: 20px;
}

nav a {
    padding: 5px;
    color: white;
    transition: 1s;
}

nav a:visited {
    color: white;
}

nav a:hover {
    color: lightgreen;
}

</style>