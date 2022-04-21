<template>
    <div class="float-right" id="Main">
        <b-container id="container" v-if="show">
            <h1>Login</h1>
            <b-form class="m-5 login">
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
    width:50%;
    text-align:center;
    background: #004AAD
}
#container {
    margin-top:25vh
}
#container h1 {
    color: #fff;
}
#container p {
    cursor:pointer;
    color:#fff
}
#container p:hover {
    color:#ccc
}
#container form button {
    background-color:rgba(1, 74, 173,.5);
    width:250px;
    font-size:1.2rem;
    border-radius:15px;
    /* border:none */
}

/* Smartphone */
@media screen and (max-width:428px) {
    #Main {
        width:100%;
        height:80vh;
    }
    #container {
        margin-top:0px
    }
    #container h1 {
        margin-top:25px;
    }
    .login input {
        width:250px
    }
}

</style>