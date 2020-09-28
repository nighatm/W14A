<template>
    <div>
        <p>{{snakeJoke}}</p>
    </div>
</template>

<script>
    export default {
        name:"snake-joke",
        computed:{
            snakeJoke: function(){
                return this.$store.getters.snakeJoke;
            }
        }
       
    }
</script>

<style scoped>

</style>