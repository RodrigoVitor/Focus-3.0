<template>
    <div class="container mt-5" id="Main">
        <!-- title of rewards -->
        <b-row>
            <b-col cols="4">
                <p>Nome da recompensa</p>
            </b-col>
            <b-col>
                <p>Valor</p>
            </b-col>
        </b-row>
        <hr class="divider-main">

        <!-- showing rewards -->
        <b-row class="mt-4">
            <b-col>
                <p>Assistir serie de noite</p>
            </b-col>
            <b-col>
                <p>50xp</p>
            </b-col>
            <b-col>
                <b-button>Comprar</b-button>
                <span><ion-icon name="trash-outline"></ion-icon></span>
            </b-col>
        </b-row>

        <hr class="divider">

        <b-row class="mt-4">
            <b-col>
                <p>Descansar na parte da tarde</p>
            </b-col>
            <b-col>
                <p>50xp</p>
            </b-col>
            <b-col>
                <b-button>Comprar</b-button>
                <span><ion-icon name="trash-outline"></ion-icon></span>
            </b-col>
        </b-row>

        <hr class="divider">

        <b-row class="mt-4">
            <b-col>
                <p>Jogar bola com os amigos</p>
            </b-col>
            <b-col>
                <p>50xp</p>
            </b-col>
            <b-col>
                <b-button>Comprar</b-button>
                <span><ion-icon name="trash-outline"></ion-icon></span>
            </b-col>
        </b-row>

        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
        <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
    </div>
</template>

<style scoped>
div#Main {
    min-height:70vh
}
hr.divider-main {
    border-top:3px solid #000
}
button {
    width:100px;
    font-size:16px;
    background-color:#004AAD;
    border:none;
    border-radius:15px
}
button:hover {
    background-color:rgb(5, 5, 199)
}
ion-icon {
    color: red;
    font-size:26px;
    cursor:pointer;
}
ion-icon:hover {
    color:darkred
}
</style>