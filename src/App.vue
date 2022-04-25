<template>
  <div id="app">
     <header>
            <div class = "container">
                 <v-row
                 align="center"
                 justify="space-around"
                 style = "margin: 0 -5px"
                 >
                     <div class="text-center">
                      <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoprof"
                      >
                      Профориентатор
                     </v-btn>
                   <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoyscd"
                      >
                      Уровень соотношения<br> "ценности-доступности
                     </v-btn>
                    <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotolaz"
                      >
                      Копинг-тест <br>Лазаруса
                     </v-btn>
                   <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotopb"
                      >
                      Психологическая<br> безопастность
                     </v-btn>
                    <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoother"
                      >
                      Прочее
                     </v-btn>
                     </div>
                   </v-row>
            </div>
     </header>
             <hr>
             <div v-if = "showblock === 'prof'" > 
                <header>
            <div class = "container">
                <v-row
                 align="center"
                 justify="space-around"
                 margin = "0 -5px"
                 >
                  <div class="text-center">
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoint"
                      >
                      Интересы
                     </v-btn>
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoiq"
                      >
                      Интеллект
                     </v-btn>
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotopersch"
                      >
                      Личностные<br>характеристики
                     </v-btn>
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gototrainprog"
                      >
                      Тренинговые<br> программы
                     </v-btn>
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoaptlearn"
                      >
                      Склонность к <br> обучению
                     </v-btn>
                     </div>
                </v-row>
            </div>
                </header>
               
                  </div>
     <hr v-if = "showblock === 'prof'">
    <div  v-if = "showblock === 'other'">
       <header>
            <div class = "container">
              
                 <v-row
                 align="center"
                 justify="space-around"
                 margin = "0 -5px"
                 ><div class="text-center">
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoforlang"
                      >
                      Иностранные <br> языки
                     </v-btn>
                     <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                      background-color = "#e4e4e4"
                      elevation="1"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoprojd"
                      >
                      Проектная <br> деятельность
                     </v-btn>
                      <v-btn
                      class="ma-2"
                      color="#f8f9fa"
                       elevation="1"
                      background-color = "#e4e4e4"
                      style = "margin: 3 8px; font-size: 12px"
                      @click = "gotoege"
                      >
                      ЕГЭ
                     </v-btn>
                     </div>
                 </v-row>
            </div>
       </header>
    </div> <hr  v-if = "showblock === 'other'" >
    <section v-if = "showcharts === 'int'">
     <RadarChart/>  
     <!-- <AreaChart1/>  -->
    <!-- <BarChart1/>
    <LineChart/>   -->
    </section>
    <section v-if = "showcharts === 'iq'">
   <RadarChart3/>  </section>
   <section  v-if = "showcharts === 'persch'">
    <RadarChart2/> </section>
    <section  v-if = "showcharts === 'trainprog'">
    <RadarChart5/> </section>
    <section  v-if = "showcharts === 'aptlearn'">
    <RadarChart4/> </section>
    <section  v-if = "showcharts === 'yscd'">
    <RadarChart1/> 
    <!-- <AreaChart/> -->
    <!-- <LineChart1/>  -->
    </section>
    <section  v-if = "showcharts === 'laz'">
    <RadarChart6/> 
    </section>
    <section v-if = "showcharts === 'pb'">
      <h4>Шкала базисных убеждений </h4>
      <AreaChart2/>
       <h4>Способы совладающего поведения</h4>
      <AreaChart4/>
       <h4>Стиль саморегуляции поведения </h4>
      <AreaChart3/>
    </section>
    <div style = "text-align: center">
    <section v-if = "showcharts === 'ege'">
      <Tableege/>
    </section>
    </div>
  </div>
</template>

<script>
import AreaChart from "./components/AreaChart.vue";
import Tableege from "./components/Tableege.vue";
import AreaChart1 from "./components/AreaChart1.vue";
import PieChart from "./components/PieChart.vue";
import BarChart from "./components/BarChart.vue";
import BarChart1 from "./components/BarChart1.vue";
import RadarChart from "./components/RadarChart.vue";
import RadarChart1 from "./components/RadarChart1.vue";
import RadarChart2 from "./components/RadarChart2.vue";
import RadarChart3 from "./components/RadarChart3.vue";
import RadarChart4 from "./components/RadarChart4.vue";
import RadarChart5 from "./components/RadarChart5.vue";
import RadarChart6 from "./components/RadarChart6.vue";
import LineChart from "./components/LineChart.vue";
import LineChart1 from "./components/LineChart1.vue";
import AreaChart2 from "./components/AreaChart2.vue";
import AreaChart3 from "./components/AreaChart3.vue";
import AreaChart4 from "./components/AreaChart4.vue";

export default {
  name: "App",
  el: "#app",
  components: {
    AreaChart,
    AreaChart1,
    PieChart,
    BarChart,
    BarChart1,
    RadarChart,
    RadarChart1,
    RadarChart2,
    RadarChart3,
    RadarChart4,
    RadarChart5,
    RadarChart6,
    LineChart,
    LineChart1,
    Tableege,
    AreaChart2,
    AreaChart3,
    AreaChart4
  },
  data:() => ({
      showblock: "nothing",
      showcharts: "nothing",
  }),
  methods:{
    gotoprof: function (){
      this.showblock = 'prof'
    },
    gotoyscd: function (){
      this.showblock = "yscd",
        this.showcharts = "yscd"
    },
    gotoother: function (){
      this.showblock = "other"
    },
    gotolaz: function (){
       this.showblock = "laz",
       this.showcharts = "laz"
    },
    gotoege: function (){
      this.showcharts = "ege"
    },
    gotopb: function (){
      this.showcharts = "pb"
    },
    gotoint: function(){
      this.showcharts = 'int'
    },
     gotoiq: function(){
      this.showcharts = "iq"
    },
    gotopersch: function(){
     this.showcharts = "persch"
    },
    gototrainprog: function(){
      this.showcharts = "trainprog"
    },
    gotoaptlearn: function(){
      this.showcharts ="aptlearn"
    },
    gotoforlang: function(){
      this.showcharts ="forlang"
    },
    gotoprojd: function(){
     this.showcharts = "projd"
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #231f1f;
  margin-top: 30px;
}
.v-btn{
  background-color: "#eeeded"!important;
  margin: 3px 8px;
  font-size: 12px;
}
.py-3{
    padding-top: -10rem!important;
}
</style>
