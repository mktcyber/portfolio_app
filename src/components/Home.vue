<template>
  <div>
    <div class="p-3 mb-2 bg-dark text-white">
        <div class="container">
            <div class="row justify-content-start">
                <div class="col-md-6">
                    <h1>Hi I'm </h1>
                    <h2>Modou K</h2>
                    <div class="title-wrapper">
                        <h3>Software Developer</h3>
                    </div>
                </div>
                <div class="col-md-2 offset-md-2">
                    <img :src="image" class="rounded-circle" width ="400" height ="400">
                </div>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomePage',
   
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
.col-md-2 {
    margin-top: 100px;
}
.row {
   display: flex;
   justify-content: space-around;
   
}
.col-md-6{
    margin-right: 2px;
    
}
.col-md-6{
    margin-top: 120px;
   
}
h1 {
  margin: 0;
  font-weight: 300;
  font-size: clamp(32px, 4vw, 52px);
  margin-right: 480px;
}
h2 {
  margin: 0;
  font-size: clamp(62px, 8vw, 140px);
  font-weight: 700;
  
}

h3 {
  text-align: center;
  font-size: clamp(20px, 2.8vw, 25px);
  margin: 0;
  font-weight: 700;
}
.title-wrapper {
  cursor: pointer;
  margin-top: 1.4em;
  padding: 1em;
  width: 100%;
  background-color: white;
  color: #1c1c1c;
  transition: all 0.2s ease-in-out;
  z-index: 2;
  border-radius: 50px;
  }
  .title-wrapper:hover {
  background-color: #23c481;
}
</style>
<!-- Add "scoped" attribute to limit CSS to this component only -->

