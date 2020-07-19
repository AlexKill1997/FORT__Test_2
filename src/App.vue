<template>
  <div id="app">
    <div class="container-fluid">
      <div class="row no-gutter">
        <div class="sidebar col-3 col-sm-3 col-md-3 col-lg-2">
          
          <sidebar/>
        </div>
        <div class="col-9 col-sm-9 col-md-9 col-lg-10">
          <top/>
          <div class="maincontent">
            <div class="first__row">
              <graph/>
              <statistics/>
            </div>
            <div class="second__row">
              <worldmap/>
              <help/>
            </div>

          </div>
        </div>
        
        
      </div>
    </div>
  </div>
</template>

<script>

import sidebar from "./components/sidebar.vue";
import top from "./components/top.vue"
import graph from "./components/graph"
import statistics from "./components/statistics"
import worldmap from "./components/worldmap.vue"
import help from "./components/help"

export default {
  name: "App",
  components: {
    sidebar,
    top,
    graph,
    statistics,
    worldmap,
    help
  }
};
</script>

<style lang="scss">

@mixin tablets {
    @media screen and (max-width: 768px) {
        @content;
    }
}

@mixin phones {
    @media screen and (max-width: 480px) {
        @content;
    }
}

html,body{
  box-sizing: border-box;
  font-size: 10px;
  @include tablets {
        font-size: 8px;
    }
    @include phones {
        font-size: 4px;
    }
 
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;

}
.sidebar{
  background-color: #1e2933;
}


li{
  list-style: none;
}

ul{
  padding-inline-start: 0;
}

.no-gutter > [class*='col-'] {
    padding-right:0;
    padding-left:0;
}

h6{
  margin:0;
}

.maincontent{
  background-color: #f9f9fa;
  width: 100%;
  
  
}

.first__row{
  display: flex;
  padding-top: 3.6rem;
  padding-left: 3%;
  @include tablets {
       display: flex;
       flex-direction: column;
       margin-bottom: 2rem;
       
    }
    
}

.second__row{
  display: flex; 
  padding-left: 2%; 
  padding-bottom: 20rem;
   @include tablets {
       display: flex;
       flex-direction: column;
       
    }
}
</style>
