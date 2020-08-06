<!-- html 시작 -->
<div id="app">
  <v-app id="inspire">
      <div>
      <v-row no-gutters>
      <v-card color="black" width="100%">
        <div style='text-align:center'>
          <span class="time">2020-03-14 12:00:00</span>
        </div>
      </v-card>
      <v-responsive width="100%"></v-responsive>
        <template v-for="item in machine">
  <v-col :key="item.idx">
    <v-card>
      <v-row>
        <v-toolbar dense flat color="#b5b5b5" height="120">
          <span class="f_mname">{{item.mid}}</span>
          <v-spacer></v-spacer>
          <span class="f_p">{{item.process}}</span>
        </v-toolbar>
      </v-row>
      <div class="text-center">
        <span class="f_end" style="align:center">{{item.timer}}</span>
      </div>
      <v-footer :fixed="true" height="100" absolute class="white">
        <v-row>
          <v-progress-linear
            value="30"
            height="100"
            color="green"
            background-color="#828282"
            rounded
          >
            <v-flex style="maxWidth:20px"></v-flex>
            <span class="vt">{{ item.count}}</span>
            <v-spacer></v-spacer>
            <span class="vt">
              <div class="text-right">{{ item.fTime }}</div>
            </span>
            <v-flex style="maxWidth:20px"></v-flex>
          </v-progress-linear>
        </v-row>
      </v-footer>
    </v-card>
  </v-col>
</template>
  </v-app>
</div>

<!-- html 끝 -->

<!-- style 시작 -->

@media all and (min-width:768px) and (max-width:4000px) {  
  
  .time{
	font-size: 8vw;
	color: #f4fc03;
	text-align: center;
  
}
.f_mname{
  position:relative;
  bottom: 28px;
  margin: 0;
  padding: 0;
  font-weight: bold;
	font-size: 3vw;
}
.f_p {
   position:relative;
   right: 18%;
	font-size: 4vh;
  color: yellow;
  display: inline-block; width: 200px; white-space: nowrap;
  margin: 0;
  padding: 0;
  
}
.vt {
	font-size: 1.2500vw;
	color: #ffffff;
}
.f_end {
  font-weight: bold;
	position:relative;
  top: 110px;
	font-size: 6.9vw;
} 

  .row {
  display: flex;
  margin-bottom: 8px;
  
  } 
  .col {
  width: 50px;
  flex-basis: 0;
  flex-grow: 1;
  flex-basis: 30%;
}
 div.v-toolbar__content {
   padding: 20px;
   margin-top: 30px;
   height: 200px;
  
   
  }
  
  div.text-center {
   height: 100vh;
   
  }
  
  
}


@media all and (min-width:768px) and (max-width:1023px) { 
.time{
	font-size: 8vw;
	color: #f4fc03;
	text-align: center;
}
.f_mname{
 position:relative;
  bottom: 28px;
  margin: 0;
  padding: 0;
  font-weight: bold;
	font-size: 3vw;
}
.f_p {
	 position:relative;
  right: 25%;
	font-size: 2vw;
  color: yellow;
  display: inline-block; width: 200px; white-space: nowrap;
  padding: 3px;
  margin: 0;
}
.vt {
	font-size: 1.2500vw;
	color: #ffffff;
}
.f_end {
  font-weight: bold;
	position:relative;
  top: 110px;
	font-size: 6.9vw;
}
  
  .row {
  display: flex;
  margin-bottom: 8px;
  
  } 
  
  .col {
  width: 50px;
  flex-basis: 0;
  flex-grow: 1;
  flex-basis: 30%;
}
  div.v-toolbar__content {
   padding: 20px;
   margin-top: 30px;
   height: 200px;
  
   
  }
  
  div.text-center {
   height: 100vh;
   
   
  }
  
}


@media all and (min-width:480px) and (max-width:767px) { 
.time{
  font-size: 8vw;
	color: #f4fc03;
	text-align: center;
}
.f_mname{
  position:relative;
  bottom: 28px;
  margin: 0;
  padding: 0;
  font-weight: bold;
	font-size: 3vw;
}
.f_p {
	 position:relative;
  right: 25%;
	font-size: 2vw;
  color: yellow;
  display: inline-block; width: 200px; white-space: nowrap;
  padding: 3px;
  margin: 0;
}
.vt {
	font-size: 1.2500vw;
	color: #ffffff;
}
.f_end {
   font-weight: bold;
  position:relative;
  top: 110px;
	font-size: 6.9vw;
}
  
 .row {
  display: flex;
  margin-bottom: 8px;
  
  } 
  
  .col {
   width: 50px;
  flex-basis: 0;
  flex-grow: 1;
  flex-basis: 30%;
}
 
  div.v-toolbar__content {
   padding: 20px;
   margin-top: 30px;
   height: 200px;
  
   
  }
  div.text-center {
  height: 100vh;
  }
  
  
}




<!-- style 끝 -->

<!-- js 시작 -->
new Vue({
  el: '#app',
  vuetify: new Vuetify(),
  data () {
    return {
      tab: null,
      machine: [
        {
          mid : 'Puma280',
          idx : 1,
          process : 'CS98D25H49-01-2',
          timer : '가공완료',
          count : '100/100',
          fTime : '0 시간 6 분',
          
        },
        {
          mid : 'PumaV400',
          idx : 2,
          process : 'O0229',
          timer : '04:34',
          count : '4/100',
          fTime : '84 시간 40 분',
          
        },
        {
          mid : 'Lynx220C',
          idx : 3,
          process : 'D580007-02-F',
          timer : '01:33',
          count : '459/500',
          fTime : '2 시간 36 분',
          
        },
        {
          mid : 'Puma240',
          idx : 4,
          process : 'WGR150D35H24-02-1',
          timer : '00:10',
          count : '70/100',
          fTime : '1 시간 31 분',
          
        },
        {
          mid : 'Lynx220CL',
          idx : 5,
          process : 'CS98D25H49-02-02',
          timer : '02:34',
          count : '12/100',
          fTime : '5 시간 0 분',
          
        },
        {
          mid : 'Lynx220SY',
          idx : 6,
          process : 'JIG-CD',
          timer : 'READY',
          count : '110/200',
          fTime : '23 시간 48 분',
          
        },
      ],
    }
  },
})


<!-- js 끝 -->

