<template>
    <div class="block">
        click me
    </div>
</template>

<script>
export default {
    props: ['delay']
}
</script>

<style scoped>
.block {
    width: 200px;
    border-radius: 20px;
    background: #0faf87;
    color: white;
    text-align: center;
    padding: 50px 0;
    margin: 40px auto;
}
</style>