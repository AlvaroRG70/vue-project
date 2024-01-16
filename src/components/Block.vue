<template>
    <div class="block" v-if="showBlock">
        click me
    </div>
</template>

<script>
    export default{
        props: ['delay'],
        data(){
            return{
                showBlock: false
            }
        },
        mounted() {
            console.log('component mounted')
            setTimeout(() => {
                this.showBlock = true
                console.log(this.delay)
            }, this.delay)
        },
        updated(){
            
        }
    }
</script>

<style>
    .block{
        width: 400px;
        background: lightblue;
        color: black;
        border-radius: 20px;
        text-align: center;
        padding: 100px 0;
        margin: 50px auto;

    }
</style>