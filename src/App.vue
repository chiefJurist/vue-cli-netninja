<template>
    <h1>{{ title }}</h1> <br>
    <p>Welcome...</p>
    <teleport to=".modals" v-if="showModal">
        <!--Here we are using the teleport component to teleport to the place with the class of 'modals'-->
        <!--You can also use ids and not only classes-->
        <Modal @close="toggleModal">
            <template v-slot:links>
                <a href="#">Sign up now!</a>
                <a href="#">more info</a>
            </template>
            <h1>Sign up for the Giveaway!</h1>
            <p>Grab your ninja swag for half price!</p>
        </Modal>
    </teleport>
    <button @click.alt="toggleModal">open modal (alt)</button><br><br>
</template>

<script>
    import Modal from "./components/Modal.vue"

    export default {
        name: 'App',
        components: { Modal },
        data(){
            return{
                title: 'My First Vue App :)',
                showModal: false,
            }
        },
        methods:{
            toggleModal(){
                this.showModal = !this.showModal
            }
        }
    }
</script>

<style>
    #app, .modals {
        /**We are adding the class modals. This way, the styles will also apply to components rendered in this div  */
        /**Note that another way to fix this is by placing the styles in the global css */
        font-family: Avenir, Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
        margin-top: 60px;
    }
    h1{
        border-bottom: 1px solid #ddd;
        display: inline-block;
        padding-bottom: 10px;
    }
</style>
