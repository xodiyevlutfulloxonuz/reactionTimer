<template>
   <div>
        <p> Reaction Time: {{score}}</p>
    <p class="rank">{{result}}</p>
   </div>
</template>
<style scoped>
.rank{
    font-size: 1.4rem;
    color: teal;
    font-weight: bold;
}
</style>

<script>
export default {
   props:['score'],

   data(){
       return{
         result:null
       }
   },
   mounted(){
       if(this.score<300){
           this.result="Powerful fingers 👍"
       }
       else if(this.score<500){
           this.result="Middle fingers"
       }
       else{
           this.result="Snail fingers"
       }
    
   }
}
</script>
