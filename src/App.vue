<template>
  <div id="nav">
    <router-link to="/">Home</router-link> | 
    <router-link to="/example2">Purpose</router-link> |
    <router-link to="/example3">Concept</router-link> |
    <router-link to="/example4">Classes</router-link> |
    <router-link to="/example5">Date</router-link>

  
  <router-view :key="$route.fullPath"/>
  </div>
</template>
<script>
  import P5 from 'p5';
export default {
   data() {
    return {
      p5Canvas: null,
    }
  },
  created() {
    const sketch = p5 => {
        

        let w = window.innerWidth;
        let h = window.innerHeight;

        p5.setup = () => {
            p5.createCanvas(w, h, p5.WEBGL);
        };

        p5.draw = () => {
            p5.background(250);
            p5.rotateY(p5.frameCount * 0.01);
            
            for (let j = 0; j < 5; j++) {
              p5.push();
              for (let i = 0; i < 80; i++) {
                p5.translate(
                  p5.sin(p5.frameCount * 0.001 + j) * 100,
                  p5.sin(p5.frameCount * 0.001 + j) * 100,
                  i * 0.1
                );
                p5.rotateZ(p5.frameCount * 0.002);
                p5.push();
                p5.sphere(8, 6, 4);
                p5.pop();
              }
              p5.pop();
            }

        };
    }

    this.p5Canvas = new P5(sketch, 'p5Canvas');
  },
  unmounted () {
    this.p5Canvas = null;
  },
}
</script>

<style>
body{
  margin:0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  top: 0px;
  text-align:right;
  font-size:25px;
  color: #2c3e50;
  position:absolute
}

#nav {
  width:100vw;
  position:relative;
  padding:0;
  z-index: 999;
  background-color:black;
}

#nav a {
  font-weight: bold;
  color: #ebeff3;
  z-index: 99;
  top:0px;
}

#nav a.router-link-exact-active {
  top:0px;
  color: #ffffff;
  z-index: 99;
}
</style>
