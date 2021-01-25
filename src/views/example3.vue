<template>
<div>
    <div align="center">
      <el-carousel :interval="5000" type="card" height="500px" >
       <el-carousel-item v-for="item in newpicture" :key="item">
         <div class="demo-image">
           <div class="block">
             <el-image
                  style="width: 700px; height: 500px;"
                  :src ="item.src"
                  fit="cover"></el-image>
           </div>
         </div>
          <p class="newtitle">{{item.title}}</p>
          <p class="newword">{{item.word}}</p>
       </el-carousel-item>
      </el-carousel>
    </div>
  <div class="Concept">Concept</div>
  <div class="Conceptcontent">光合玻璃藝術創始的初衷是引進國外玻璃專門技術，在國內以教育推廣的方式分享技法經驗給有興趣學習的人。引進的方式為個人出國學習或邀請國外藝術家來教，近幾年結合個人在公共藝術委製案中習得的經驗，融入教學內容，讓學生能盡快的學以致用，希望結業的學員能與我一起接單創作，這才是真正的教育推廣。</div>
  <div class="background"></div>
</div>
</template>
<script>
export default {
  name: 'hello',
  data(){
    return{
    newpicture:[
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12473503_929475133799322_75270033382668818_o.jpg",
        title : "",
        word : " "},
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/10710663_713632045383633_7796167457212718845_n.jpg",
        title : "",
        word : ""},
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12186752_901093876637448_7787609638407932294_o.jpg",
        title:"",
        word:""},
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
    position:relative;
    width:90vw;
    top:200px;
    padding-top: 100px;
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
    left: 570px;
    top: 25px;
    font-family: Roboto;
    font-style: italic;
    font-weight: normal;
    font-size: 40px;
    line-height: 83px;
    text-align: center;
    color: #ffffff;
  }
  .Conceptcontent {
    position: absolute;
    width: 884px;
    height: 180px;
    left: 320px;
    top: 118px;
    font-family:Roboto;
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 28px;
    text-align: center;
    letter-spacing: 0.2em;
    color: #ffffff;
  }
  .background {
    position: absolute;
    width:100vw;
    height:40vh;
    background-color: black;
  }

</style>