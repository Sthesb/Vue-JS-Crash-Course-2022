<template>
    <div class="backdrop">
        <div class="backdrop_modal">
            <p>Modal Content</p>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style scope>
.backdrop {
    top: 0;
    position: fixed;
    background-color: rgba(0,0,0,0.7);
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
}
.backdrop_modal {
    width: 400px;
    height: 100px;
    
    margin: 100px auto;
    background: white;
    border-radius: 10px;
    display: flex;
    align-items: center;
    justify-content: center;
}
.backdrop_modal > p {
    padding: 0px;
    margin: 0px;
}
</style>