<template>
    <div class="backdrop" @click.self="closeModal">
        <div class="backdrop_modal" :class="{ sale: theme === 'sale' }" >
            
            <slot >default content</slot>
            <div class="actions">
                <slot name="links" />
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['theme'],
    methods: {
        closeModal () {
            this.$emit('close')
        }
    }
}
</script>

<style scope>
.backdrop {
    top: 0;
    position: fixed;
    background-color: rgba(120, 110, 110, 0.7);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.backdrop_modal {
    width: 400px;
    min-height: 100px;
    padding: 20px 0;
    display: flex;
    flex-direction: column;
    margin: 100px auto;
    background: white;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.backdrop_modal > h2 {
    color: rgb(0, 217, 255);
}
.backdrop_modal > p {
    padding: 0px;
    margin: 0px;
}
.sale {
    background-color: crimson;
    color: white;
}
.sale >  h2 {
    color: white;
}
.actions > a {
    color: white;
    font-size: 20px;
    font-weight: italic ;
    margin-bottom: 20px;
}
</style>