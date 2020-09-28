<template>
    <div>
        <p> {{ loudJoke}}</p>    
    </div>
</template>

<script>

    export default {
        name:"loud-joke",
        computed:{
            loudJoke: function(){
                return this.$store.getters.loudJoke;
            }
        }
    }
</script>

<style scoped>

</style>