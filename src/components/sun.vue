<template>
    <div>
      <button @click="change">改变</button>
    </div>
</template>
<script>
    export default {
        data(){
            return {
                arr:[]
            }
        },
        props:['myarr'],
        watch:{
            myarr:{
                handler:function(val){
                  // debugger;
                    if(val.length===0){
                        this.arr = val
                        window.console.log(this.arr)
                    }else {
                        this.arr.push('12')
                        window.console.log(this.arr)
                    }

                },
                deep:true
            }
        },
        methods:{
          change(){
              this.arr.push('init');
          }
        }
    }
</script>
