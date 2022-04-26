<template>
    <div>
        <div class="container">
            <div class="row justify-content-start">
                <div class="col-md-6">
                    <img :src="image" class="rounded-circle" width ="400" height ="400">
                </div>
                <div class="col-md-2 offset-md-2">
                    find me
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    name:'FindMe',
    data(){
        return{
            image:'/assets/mkt.jpeg',
        }
    }
}
</script>
<style scoped>
    .container{
        margin-top: 100px;
        margin-bottom: 200px;
    }
</style>