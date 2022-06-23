<template>
    <p>Reaction time - {{ score }}</p>
    <p class="rank">{{ rank }}</p>
</template>

<script >
    export default{
        props: ['score'],
        data() {
            return{
                rank: null
            }
        },
        mounted() {
            if(this.score < 250){
                this.rank = 'Super-fast fingers'
            }else if (this.score < 400) {
                this.rank = 'fast fingers'
            } else{
                this.rank = 'slow fingers...'
            }
        }
    }
</script>

<style scoped>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>