<template>
    <div class="backdrop">
        <div class="modal">
            <h1>Modal Title</h1>
            <p>Modal Content</p>
        </div>
    </div>
</template>

<style scoped>
    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: white;
        border-radius: 10px;
    }
    .backdrop{
        top: 0;
        position: fixed;
        background: rgba(0, 0, 0, 0.5);
        width: 100%;
        height: 100%;
    }
    .modal h1{
        color: #03cfb4;
        border: none;
        padding: 0;
        /* Another way to prevent overiding the style in the parent component is t o be more specific about the style */
    }
    p{
        font-style: normal;
        /* Overiding a global style */
    }
</style>