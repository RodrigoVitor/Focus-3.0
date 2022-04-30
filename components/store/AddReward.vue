<template>
    <b-form class="container">
        <b-row class="mt-5 d-flex justify-content-center">
            <b-col lg="6">
                <b-form-group label="Nome da Recompensa" label-for="input-1">
                    <b-form-input id="input-1" type="text" v-model="Reward" placeholder="Ex: Assistir serie, Jogar video game, etc"></b-form-input>
                </b-form-group>
            </b-col>
            <b-col lg="6">
                <b-form-group label="Valor da Recompensa" label-for="input-2">
                    <b-form-input id="input-2" v-model="Price" type="text" placeholder="Ex:120"></b-form-input>
                </b-form-group>
            </b-col>
            <div>
                <b-button>Adicionar recompensa</b-button>
            </div>
        </b-row>
    </b-form>
</template>

<script>
import {mapState, mapMutations} from 'vuex'

export default {
    methods: {
        ...mapMutations('rewards', ['CHANGE_REWARD','CHANGE_PRICE'])
    },
    computed: {
        ...mapState('rewards', ['reward', 'price']),
        Reward: {
            get() {
                return this.reward
            },
            set(value) {
               return this.CHANGE_REWARD(value)
            }
        },
        Price: {
            get() {
                return this.price
            },
            set(value) {
                return this.CHANGE_PRICE(value)
            }
        }
    }    
}
</script>


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