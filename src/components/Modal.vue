<template>
    <div class="backdrop">
        <div class="modal">
            <p>Modal content</p>
        </div>
    </div>
</template>


<style>
    .modal{
        width: 400px;
        padding: 20px;
        margin: 100px auto;
        background: whitesmoke;
        border-radius: 10px;
    }
    .backdrop{
        top: 0;
        position: fixed;
        background: rgba(0,0,0,0.5);
        width: 100%;
        height: 100%;
    }
</style>