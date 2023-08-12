<template>
    <h1>{{ title }}</h1> <br>
    <input type="text" ref="name">
    <button @click="handleClick">Click Me</button>
    <!--The template ref here was used to grip an element just like the query selector-->
</template>

<script>
    export default {
        name: 'App',
        data(){
            return{
                title: 'My First Vue App :)'
            }
        },
        methods: {
            handleClick(){
                console.log(this.$refs.name),
                this.$refs.name.focus()
                //This is how to reference template refs in scripts
            }
        }
    }
</script>

<style>
    #app {
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
