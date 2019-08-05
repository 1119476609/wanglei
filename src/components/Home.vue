<template>
    <div>
      <div v-for="(item,index) in arr" key:index @click="btnc(index)">{{item}}</div>
      <li v-if="boolarr[num]">
               <span v-for="(ite,idx) in list[num]" key:idx>
                     {{ite}}
               </span>
           </li>
     <li v-else></li>
    </div>
</template>
<script>
export default {
    data(){
        return{
           list:[['1-1','1-2','1-3'],['2-1','2-2','2-3'],['3-1','3-2','3-3']],
           boolarr:[false,false,false],
           arr:['标题1','标题2','标题3'],
           num:null
        }
    },
    methods:{
        btnc(idx){
            this.boolarr[idx]=!this.boolarr[idx]
            this.boolarr=this.boolarr.map(item=>item=false)
            this.boolarr[idx]=true
            this.num=idx
            console.log(this.boolarr)
        }
    }
}
</script>
<style scoped>
 *{
     margin: 0;
     padding: 0;
     list-style: none;
 }
</style>

