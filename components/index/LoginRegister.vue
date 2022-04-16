<template>
    <div class="float-right" id="Main">
        <b-container id="container" v-if="show">
            <h1>Login</h1>
            <b-form class="m-5">
                <b-form-group>
                    <b-form-input type="email" placeholder="Digite seu email"></b-form-input>
                </b-form-group>
                <b-form-group>
                    <b-form-input type="password" placeholder="Digite sua senha"></b-form-input>
                </b-form-group>
                <p @click="showLoginRegister">Não possue uma conta? cadastra-se já!</p>
                <b-button>Entrar</b-button>
            </b-form>
        </b-container>

        <b-container id="container" v-if="!show">
            <h1>Cadastrar</h1>
            <b-form class="m-4">
                <b-form-group>
                    <b-input type="text" placeholder="Nome e Sobrenome"></b-input>
                </b-form-group>
                <b-form-group>
                    <b-input type="email" placeholder="Digite o email que deseja utilizar"></b-input>
                </b-form-group>
                <b-form-group>
                    <b-input type="password" placeholder="Digite sua senha">Digite sua senha</b-input>
                </b-form-group>
                <b-form-group>
                    <b-input type="password" placeholder="Confirmar senha"></b-input>
                </b-form-group>
                <p @click="showLoginRegister">Ja possue uma conta? Então faça seu login!</p>
                <b-button>Cadastrar</b-button>
            </b-form>
        </b-container>
    </div>
</template>

<script>
export default {
    data () {
        return {
            show: true
        }
    },
    methods: {
        showLoginRegister() {
            this.show = !this.show
        }
    }
}
</script>

<style scoped>
#Main {
    height:100vh;
    width:50vw;
    text-align:center;
    background: #FBFF2D
}
#container {
    margin-top:25vh
}
#container h1 {
    color: #004aad;
}
#container p {
    cursor:pointer
}
#container p:hover {
    color:blue
}
#container form button {
    background-color:#004aad;
    width:250px;
    font-size:1.2rem
}

</style>