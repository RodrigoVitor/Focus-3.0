<template>
    <div>
        <b-container>
            <b-form class="mt-5">
                <b-form-group>
                    <b-input type="text" placeholder="Adicione uma tarefa. Ex: Estudar inglês"></b-input>
                </b-form-group>
                <div class="d-flex justify-content-center">
                    <b-button variant="success">Adicionar</b-button>
                </div>
            </b-form>

            <b-row class="mt-5">
                <b-col lg="10" sm="6">
                    <p>Estudar para prova de inglÊs</p>
                </b-col>
                <b-col lg="1"  sm="1">
                    <a href="#" class="delete-icon"><ion-icon name="trash-outline" size="large"></ion-icon></a>
                </b-col>
                <b-col lg="1" sm="1">
                    <a href="#"><ion-icon name="checkmark-done-outline" size="large"></ion-icon></a>
                </b-col>
            </b-row>
            <b-row class="mt-5">
                <b-col lg="10">
                    <p>Estudar javascript as 9h</p>
                </b-col>
                <b-col lg="1">
                    <a href="#" class="delete-icon"><ion-icon name="trash-outline" size="large"></ion-icon></a>
                </b-col>
                <b-col lg="1">
                    <a href="#"><ion-icon name="checkmark-done-outline" size="large"></ion-icon></a>
                </b-col>
            </b-row>
            <b-row class="mt-5">
                <b-col lg="10">
                    <p>Passear com o dog</p>
                </b-col>
                <b-col lg="1">
                    <a href="#" class="delete-icon"><ion-icon name="trash-outline" size="large"></ion-icon></a>
                </b-col>
                <b-col lg="1">
                    <a href="#"><ion-icon name="checkmark-done-outline" size="large"></ion-icon></a>
                </b-col>
            </b-row>
        </b-container>

        <script type="module" src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.esm.js"></script>
        <script nomodule src="https://unpkg.com/ionicons@5.5.2/dist/ionicons/ionicons.js"></script>
    </div>
</template>

<style scoped>
.delete-icon {
    color: red
}
button {
    width:250px;
    background-color:#004AAD;
    border:none;
    border-radius:15px
}
button:hover {
    background-color:rgb(5, 5, 199)
}

/* tablet */ 
@media screen and (max-width: 834px) {
    div {
        margin: 0 0 150px 0;
    }
}
</style>