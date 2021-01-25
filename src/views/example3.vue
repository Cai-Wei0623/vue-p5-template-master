<template>
<el-carousel :interval="4000" type="card" height="800px" >
       <el-carousel-item v-for="item in newpicture" :key="item">
         <div class="demo-image">
           <div class="block">
             <el-image
                  style="width: 750px; height: 500px;"
                  :src ="item.src"
                  fit="cover"></el-image>
           </div>
         </div>
          <p class="newtitle">{{item.title}}</p>
          <p class="newword">{{item.word}}</p>
       </el-carousel-item>
      </el-carousel>
  <div class="Concept">Concept</div>
  <div class="Conceptcontent">光合玻璃藝術創始的初衷是引進國外玻璃專門技術，在國內以教育推廣的方式分享技法經驗給有興趣學習的人。引進的方式為個人出國學習或邀請國外藝術家來教，近幾年結合個人在公共藝術委製案中習得的經驗，融入教學內容，讓學生能盡快的學以致用，希望結業的學員能與我一起接單創作，這才是真正的教育推廣。</div>
</template>
<script>
export default {
  name: 'hello',
  data(){
    return{
    newpicture:[
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/10/banner.png",
        title : "",
        word : " 「當藝術碰撞科技，會迸出什麼樣的火花呢?」"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2019/10/board-2303325_1920.jpg",
        title : "2020藝術學院學士班春之清華獎學金",
        word : "【獲獎名單】"},
      { src : "https://ipta.nthu.edu.tw/wp-content/uploads/2020/05/tfho.jpg",
        title:"《科技物件與人類幻象》",
        word:"【講座與工作坊】"},
    ],
    }
},
}
</script>
<style>
  .el-carousel-item{
    position: absolute;
    font-size: 14px;
    line-height: 200px;
    top: 500px;
    margin: 0;
    Z-index:99999;
  }
  .el-carousel{
    top:200px;
  }
  .newtitle {
    color: #ECAA65;
    font-size:20px; 
  }
  .newword {
    color: #ECAA65;
    font-size:18px;
  }
  .Concept {
    position: absolute;
    width: 372px;
    height: 100px;
    left: 540px;
    top: 25px;
    font-family: Roboto;
    font-style: italic;
    font-weight: normal;
    font-size: 45px;
    line-height: 83px;
    text-align: center;
    color: #ffffff;
  }
</style>