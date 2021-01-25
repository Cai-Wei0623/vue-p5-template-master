<template>
<div>
    <div align="center">
      <el-carousel :interval="5000" type="card" height="700px" >
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

  <div class="Classes">Classes</div>
  <div class="background"></div>
</div>
</template>
<script>
export default {
  name: 'hello',
  data(){
    return{
    newpicture:[
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12045350_889323761147793_2458868865881052802_o.jpg",
        title : "體驗課",
        word : "歡迎團體預約報名(十人以上開班)"},
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12138465_891907170889452_6906923417979540628_o.jpg",
        title : "《玻璃初體驗》-【基礎點線面體驗課】",
        word : "打造屬於自己的玻璃盤"},
      { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12363259_921671947912974_668965375217201905_o.jpg",
        title:"基礎技法課",
        word:"【吊飾】曲線/圓形切割"},
         { src : "https://raw.githubusercontent.com/Cai-Wei0623/vue-p5-template-master/main/src/photo/12615377_942667075813461_1706611992036668603_o.jpg",
        title : "基礎技法課",
        word : "【玻璃盤】直線切割"},
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
    padding-top: 0px;
  }
  .newtitle {
    color: #ECAA65;
    font-size:20px; 
  }
  .newword {
    color: #ECAA65;
    font-size:18px;
  }
  .Classes {
    position: absolute;
    width: 372px;
    height: 100px;
    left: 570px;
    top: 50px;
    font-family: Roboto;
    font-style: italic;
    font-weight: normal;
    font-size: 40px;
    line-height: 83px;
    text-align: center;
    color: #ffffff;
  }
  .background {
    position: absolute;
    width:100vw;
    height:40vh;
    background-color: black;
  }
.el-carousel__item--card, .is-in-stage{
    background-color:black;
}
</style>