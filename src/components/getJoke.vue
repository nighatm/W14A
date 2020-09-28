<template>
    <div>
        <h4>Assignment W14A Vue Axios</h4>
        <br>
    <button @click="getJoke"> Get the Joke!</button>  
    <br>
    <div>
        <button @click="updatejoketype('loud')"> Make it Loud</button>
        <button @click="updatejoketype('snake')"> Make it Snake</button>
        <button @click="updatejoketype('normal')"> Make it Normal</button>


    </div>      

    </div>
</template>

<script>
import axios from "axios"
    export default {
        name: "get-joke",

        //  data() {
        //     return {
        //         joke: ""
        //     }
        // },
        methods: {
            getJoke: function(){
                axios.request({
                    url:"https://geek-jokes.sameerkumar.website/api?format=json",
                    method:"GET"
                }).then((response) => {
                    console.log(response);
                   this.$store.commit("updateJoke", response.data.joke)
                  //  this.joke = response.data.joke
                }).catch((error) => {
                    console.log(error);
                    this.joke = "Something went Wrong...";

                });

            },
            updatejoketype: function(type){
                this.$store.commit("updateJokeType", type);
            }
        },
    }
</script>

<style lang="sass" scoped>

</style>