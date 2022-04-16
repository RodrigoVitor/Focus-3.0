<template>
    <div>
        <b-container class="bv-example-row float-left d-flex justify-content-center align-items-center" id="container">
            <b-row>
                <b-col>
                    <img src="/img/logo.png" alt="logo focus" id="logo-image">
                </b-col>
            </b-row>
            <b-row>
                <b-col>
                    <img src="/img/readbook.png" alt="menino lendo livro" id="book-image">
                </b-col>
            </b-row>
            <b-row class="m-5">
                <p>Para ter foco é preciso ter disciplina</p>
            </b-row>
        </b-container>
    </div>
</template>

<style scoped>
#container {
    width:50vw;
    height:100vh;
    background: #FBFF1A;
    flex-direction: column;
}
#container .row p {
    color:#004AAD;
    font-weight:bold
}
</style>