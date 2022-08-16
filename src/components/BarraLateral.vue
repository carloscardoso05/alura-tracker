<template>
    <header>
        <h1>
            <img src="../assets/logo.png" alt="logo">
        </h1>
        <button class="button btn-modo-escuro" @click="alterarTema">{{textoBotao}}</button>
    </header>
</template>

<script lang="ts">
    import { defineComponent } from 'vue';

    export default defineComponent({
        name: 'BarraLateral',
        data () {
            return {
                modoEscuroAtivo: false
            }
        },
        computed: {
            textoBotao () {
                if(this.modoEscuroAtivo){
                    return 'Desativar modo escuro'
                } else {
                    return 'Ativar modo escuro'
                }
            }
        },
        emits: ['aoTemaAlterado'],
        methods: {
            alterarTema () {
                this.modoEscuroAtivo = !this.modoEscuroAtivo
                // this.$emit('aoTemaAlterado', this.modoEscuroAtivo)
                this.$emit('aoTemaAlterado')
            }
        }
    })
</script>

<style scoped>
    header {
        padding: 1rem;
        background: #0d3b66;
        width: 100%;
        height: 100vh;
        text-align: center;
    }
    .btn-modo-escuro{
        margin: 1rem;
    }
    @media only screen and (max-width: 768px) {
        header {
            padding: 2.5rem;
            height: auto;
        }
    }
</style>