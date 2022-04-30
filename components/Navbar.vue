<template>
    <div id="Main">
        <b-navbar toggleable="lg" class="d-flex" type="dark"  id="nav">
            <b-navbar-brand href="#">Rodrigo Vitor <span>0xp</span></b-navbar-brand>

            <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

            <b-collapse id="nav-collapse" is-nav>

            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto">
                <NuxtLink to="/home">Home </NuxtLink>
                <NuxtLink to="/store">Loja </NuxtLink>
                <NuxtLink to="/my-rewards">Meu Estoque </NuxtLink>
                <NuxtLink to="/">Logout </NuxtLink>
            </b-navbar-nav>
            </b-collapse>
        </b-navbar>
    </div>
</template>

<style scoped>
#Main {
    min-height:20px;
}
#nav {
    background-color: #004AAD;
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