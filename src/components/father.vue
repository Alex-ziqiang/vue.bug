<template>
    <div class="demo">
        <button @click="del">删除全部</button>
        <demo :myarr="arr"></demo>
    </div>
</template>
<script>
    import demo from './sun'
  export default {
      data(){
          return {
              arr:[]
          }
      },
      components:{demo},
      methods:{
          del(){
              this.arr=[];
          },
      }
  }
</script>
<style>
    .demo {
        width: 800px;
        height: 600px;
        margin: 100px auto;
        border: 1px solid #E5B98C;
    }
</style>