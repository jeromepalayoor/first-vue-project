<template class="no">
    <div class="backdrop" @click.self="closeModal">
        <div class="modal" :class="{ sale: theme === 'sale' }">
            <slot>Title</slot>
            <div class="actions">
                <slot name="links">Links</slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
    methods: {
        closeModal() {
            this.$emit('close')
        }
    }
}
</script>

<style>
.modal {
    width: 400px;
    padding: 20px;
    margin: 100px auto;
    background: whitesmoke;
    border-radius: 10px;
}

.modal h1 {
    color: #03cfb4;
    border: none;
    padding: 0;
}

.modal p {
    font-style: normal;
}

.modal .actions {
    text-align: center;
    margin: 30px 0 10px 0;
    color: #333;
}

.modal .actions a {
    color: #333;
    padding: 8px;
    border: 1px solid #bbb;
    border-radius: 4px;
    text-decoration: none;
    margin: 10px;
}

.backdrop {
    top: 0;
    position: fixed;
    background: rgba(0, 0, 0, 0.5);
    width: 100%;
    height: 100%;
}

.modal.sale {
    background-color: red;
    color: white;
}

.modal.sale .actions a{
    color: white;
}

.modal.sale .actions {
    color: white;
}

.modal.sale h1 {
    color: white;
}
</style>