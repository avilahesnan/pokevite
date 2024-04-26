<template>
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container-fluid">
            <router-link class="navbar-brand" to="/">
                <img src="https://cdn-icons-png.flaticon.com/128/1408/1408927.png" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
                PokeVite
            </router-link>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav">
                    <li class="nav-item">
                        <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
                    </li>
                    <li class="nav-item">
                        <router-link class="nav-link" to="/about">About</router-link>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
    <div class="main">
        <router-view></router-view>
    </div>
    <footer class="bg-dark text-light">
        <div>Design in {{ new Date().getFullYear() }}</div>
    </footer>
</template>

<style>

body {
    height: 100vh;
    background: rgb(240,251,251);
    background: linear-gradient(360deg, rgba(240,251,251,1) 0%, rgba(125,224,255,1) 50%, rgba(10,10,10,1) 100%);
}
footer {
    position: fixed;
    bottom: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 56px;
}

</style>