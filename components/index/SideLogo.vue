<template>
    <div id="Main">
        <b-container class="bv-example-row float-left d-flex justify-content-center align-items-center" id="container">
            <b-row class="mt-5">
                <b-col>
                    <img src="/img/logo-mobile.png" alt="logo focus" id="logo-image">
                </b-col>
            </b-row>
            <b-row>
                <b-col>
                    <img src="/img/readbook-mobile.png" alt="menino lendo livro" id="book-image">
                </b-col>
            </b-row>
            <b-row class="m-5">
                <p>Para ter foco é preciso ter disciplina</p>
            </b-row>
        </b-container>
    </div>
</template>

<style scoped>
#Main {
    width:50%;
}
#container {
    height:100vh;
    background: #fff;
    flex-direction: column;
}
#container .row p {
    color:#004AAD;
    font-weight:bold
}

/* SMartphone */
@media screen and (max-width:428px) {
    #Main {
        width:100vw;
    }
    #container {
        height: 350px;
    }
}
</style>