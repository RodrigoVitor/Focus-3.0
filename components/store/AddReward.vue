<template>
    <b-form class="container">
        <b-row class="mt-5 d-flex justify-content-center">
            <b-col lg="6">
                <b-form-group label="Nome da Recompensa" label-for="input-1">
                    <b-form-input id="input-1" type="text" placeholder="Ex: Assistir serie, Jogar video game, etc"></b-form-input>
                </b-form-group>
            </b-col>
            <b-col lg="6">
                <b-form-group label="Valor da Recompensa" label-for="input-2">
                    <b-form-input id="input-2" type="text" placeholder="Ex:120"></b-form-input>
                </b-form-group>
            </b-col>
            <div>
                <b-button>Adicionar recompensa</b-button>
            </div>
        </b-row>
    </b-form>
</template>

<style scoped>
button {
    width:250px;
    background-color:#004AAD;
    border:none;
    border-radius:5px
}
button:hover {
    background-color:rgb(5, 5, 199)
}
</style>