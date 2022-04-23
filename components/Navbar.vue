<template>
    <nav class="d-flex align-items-center">
        <div class="nav-item">
            <p>Rodrigo Vitor <span>0xp</span></p>
        </div>
        <div class="nav-item">
            <NuxtLink to="/home">Home </NuxtLink>
            <NuxtLink to="/store">Loja </NuxtLink>
            <NuxtLink to="/">Meu Estoque </NuxtLink>
            <NuxtLink to="/">Perfil </NuxtLink>
            <NuxtLink to="/">Logout </NuxtLink>
        </div>
    </nav>
</template>

<style scoped>
nav {
    background-color: #004AAD;
    padding:10px;
    justify-content: space-around;
}
.nav-item p {
    color:white;
    font-size:24px;
}
a {
    color:white;
    margin-right:15px;
    text-decoration: none;
    font-size:22px;
}
.nuxt-link-exact-active {
    color:#ccc
}
</style>