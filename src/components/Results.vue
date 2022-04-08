<template>
    <h4 class="mt-3">{{ result }}</h4>

</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            result: null
        }
    },
    mounted(){
        if(this.score < 300){
            this.result = "You're a G"
        }else if ( this.score >= 300  && this.score < 500){
            this.result = "You're slow. try agin my G"
        }else {
            this.result = "You're Mabhena"
        }
    }
}
</script>