<template>
    <div class="float-right" id="Main">
        <b-container id="container" v-if="show">
            <h1>Login</h1>
            <b-form class="m-5 login">
                <b-form-group>
                    <b-form-input type="email" v-model="form.email" placeholder="Digite seu email"></b-form-input>
                </b-form-group>
                <b-form-group>
                    <b-form-input type="password" v-model="form.password" placeholder="Digite sua senha"></b-form-input>
                </b-form-group>
                <p @click="showLoginRegister">Não possue uma conta? cadastra-se já!</p>
                <b-button>Entrar</b-button>
            </b-form>
        </b-container>

        <b-container id="container" v-if="!show">
            <h1>Cadastrar</h1>
            <b-form class="m-4">
                <b-form-group>
                    <b-input type="text" v-model="form.username" :state="validate.usernameState" 
                    @keyup="validate_name" placeholder="Nome e Sobrenome"></b-input>
                </b-form-group>
                <b-form-group>
                    <b-input type="email" v-model="form.useremail" :state="validate.useremailState" 
                    @keyup="validate_email" placeholder="Digite o email que deseja utilizar"></b-input>
                </b-form-group>
                <b-form-group>
                    <b-input type="password" v-model="form.userpass" :state="validate.userpassState" aria-describedby="input-live-pass"
                    @keyup="validate_pass" placeholder="Digite sua senha">Digite sua senha</b-input>
                    <b-form-invalid-feedback id="input-live-pass">
                        <span class="text-white">Sua senha precisa ter no máximo 5 caracteres</span>
                    </b-form-invalid-feedback>
                </b-form-group>
                <b-form-group>
                    <b-input type="password" v-model="form.confpass" :state="validate.confpassState" aria-describedby="input-invalid-password" 
                    @keyup="conf_pass" placeholder="Confirmar senha"></b-input>
                    <b-form-invalid-feedback id="input-invalid-password">
                        <span class="text-white">Sua senha esta diferente do qual você digitou acima</span>
                    </b-form-invalid-feedback>
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
            show: true,
            validate: {
                usernameState: null,
                useremailState: null,
                userpassState: null,
                confpassState: null
            }
        }
    },
    methods: {
        showLoginRegister() {
            this.show = !this.show
        },
        validate_name() {
            return this.form.username.length < 2 ? this.validate.usernameState = false : this.validate.usernameState = true
        },
        validate_email() {
            return this.form.useremail.length < 3 ? this.validate.useremailState = false : this.validate.useremailState = true
        },
        validate_pass() {
            return this.form.userpass.length < 5 ? this.validate.userpassState = false : this.validate.userpassState = true
        },
        conf_pass() {
            return this.form.confpass != this.form.userpass ? this.validate.confpassState = false : this.validate.confpassState = true
        }
    },
    computed: {
        form() {
            return {
                email: '',
                password: '',
                username: '',
                useremail: '',
                userpass: '',
                confpass: ''
            }
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