


<script>
  export default {
    data() {
    return({
     list: [
        '第一条数据',
        '第二条数据',
        '第三条数据',
        '第四555'
      
      ],
      text: '雷神之锤'
   })
},
methods: {
  handleClick(){
    this.list.push(this.text);
    // console.log(this.list);
    this.text=""
  },
  removeItem(index){
    this.list.splice(index,1)
  }
}

}
</script>
<template>

<div class="tou">
    
    <input type="text" v-model="text">
    <button @click="handleClick"><p>提交</p></button>
    <ul class="todo-list">
      <li v-for="(item,index) in list" 
        :key="index" 
        @click="removeItem(index)" >
        {{item}}
      </li>
    </ul>
</div>
</template>
<style>
body{
  text-align: center;
  background: #d6d6d6;
}
.tou{
  margin-top: 50px;
}
.tou p{
  color: #ffffff;
  text-align: center;
}
button{
  text-align: center;
  padding-top: 7px;
   height: 60px;
  width: 100px;
  background-color:#5FB878;
  transition: 0.5s all;
  opacity: 1;
 border-radius: 5px;
 border: 0;
 margin-left: 5px;
}
button:hover{
  transition: 1s all;
  opacity: 0.5;
}

input{
  background-color: antiquewhite;
  height: 50px;
  width: 300px;
  font-size: 20px;
}
ul{
  margin-top: 40px;
  list-style: none;
  font-size: 30px;
}
</style>
