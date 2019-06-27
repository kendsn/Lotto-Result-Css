<template>
<div class="terms-content theme1">
  <!-- Head--> 
  <div class="header">
    <div class="header_top">
      <div class="header_btnLeft">
        <div class="btn_home"></div>
        <div id="divBtn_Results" class="btn_lotteryResult"></div>
      </div>  
      <div class="header_title">北京賽車</div>
      <div class="header_btnRight">
        <div class="btn_betRecord"></div>
        <div class="btn_menu" id="btn_rightMenu"></div>
      </div>
    </div>
    <div class="headerPage_down">
      <div class="header_phase">
        <span id="spnGid" class="header_phaseNum">732031</span>期
      </div>
      <div class="header_time">
        <span>
          <span id="spnHH" class="greensp">10</span>
          <span class="greensp">：</span>
        </span>
        <span id="spnMM" class="greensp">30</span>
        <span class="greensp">：</span>
        <span id="spnSS" class="greensp">21</span>
      </div>
      <div id="fonBalance" class="header_money">0</div>
        <font id="fonNowDate" style="display: none;">GMT+8 2019-04-12 17:53:48</font>
    </div>
  </div> 
  <div class="Prev_result Hrline-botton">
    <div class="Div_result">  
      <div class="control_L">
        <span class="control_L1">732030</span><span class="control_L2">期</span>
      </div>  
      <div class="control_R">
        <div class="OpenPrize_pk10 car2">2</div>
        <div class="OpenPrize_pk10 car8">8</div>
        <div class="OpenPrize_pk10 car3">3</div>
        <div class="OpenPrize_pk10 car10">10</div>
        <div class="OpenPrize_pk10 car9">9</div>
        <div class="OpenPrize_pk10 car1">1</div>
        <div class="OpenPrize_pk10 car5">5</div>
        <div class="OpenPrize_pk10 car6">6</div>
        <div class="OpenPrize_pk10 car7">7</div>
        <div class="OpenPrize_pk10 car4">4</div>  
      </div>
    </div>
  </div>
  <!-- Body -->
  <div class="zxDiv">
    <div class="themesTab_body">
      <div class="themesTab">
        <div><button :class="{tablinks:true,active:mytabs==1}" @click="mytabs=1">London</button></div>
        <div><button class="tablinks" @click="mytabs=2">Paris</button></div>
        <div><button class="tablinks" @click="mytabs=3">Tokyo</button></div>
        <div><button class="tablinks" @click="mytabs=4">Taiwan1</button></div>
        <div><button class="tablinks" @click="mytabs=5">Taiwan2</button></div>
        <div><button class="tablinks" @click="mytabs=6">Taiwan3</button></div>
        <div><button class="tablinks" @click="mytabs=7">Taiwan4</button></div>
      </div>
    </div>
    <div class="themesBg"></div>  
    <div class="themesHead">
      <div class="tabBtn">更多</div>
    </div> 

    <!--Tabs index-->
    <div id="London" :class="{tabcontent:true,ShowMe:mytabs==1,NoShow:mytabs!=1}">
     <h3>London</h3>
    <p>London is the capital of France.</p> 
    </div>

    <div id="Paris" :class="{tabcontent:true,ShowMe:mytabs==2,NoShow:mytabs!=2}">
    <h3>Paris</h3>
    <p>Paris is the capital of France.</p> 
    </div>

    <div id="Tokyo" :class="{tabcontent:true,ShowMe:mytabs==3,NoShow:mytabs!=3}">
    <h3>Tokyo</h3>
    <p>Tokyo is the capital of Japan.</p>
    </div>

    <div id="Taiwan" :class="{tabcontent:true,ShowMe:mytabs==4,NoShow:mytabs!=4}">
    <h3>Taiwan</h3>
    <p>Taiwan is the capital of 台北.</p>
    </div>

    <div id="Taiwan" :class="{tabcontent:true,ShowMe:mytabs==5,NoShow:mytabs!=5}">
    <h3>Taiwan</h3>
    <p>Taiwan is the capital of 台中.</p>
    </div>

    <div id="Taiwan" :class="{tabcontent:true,ShowMe:mytabs==6,NoShow:mytabs!=6}">
    <h3>Taiwan</h3>
    <p>Taiwan is the capital of 台南.</p>
    </div>

    <div id="Taiwan" :class="{tabcontent:true,ShowMe:mytabs==7,NoShow:mytabs!=7}">
    <h3>Taiwan</h3>
    <p>Taiwan is the capital of 高雄.</p>
    </div>
  </div>

  <!-- Foot -->
  <div class="foot_Bet">
    <div class="foot_Btn">
      <v-btn class="le" @click='backtohome()'>清空選取</v-btn>
      <v-btn class="cv themeBtn" @click='gotodash()'><span class="btnChoose">共選了<span class="btnNum">0</span>球</span><span class="btnSub">確定送出</span></v-btn>
    </div>
  </div>
  <p></p>

  <!-- Dialog -->
  <div class="maskAll_result">
    <div class="Game_menu">
      <div class="Game_menu-close"></div>
      <div class="Game_menu-reset"></div>
      <!--head-->
      <div class="Game_menu_title">
        <div class="titleDialog">
            <span class="titleSpan">開獎結果</span>
            <span>(</span>
            <span>大眾賽車</span>
            <span>)</span>
        </div>
      </div>
      <!--body-->
      <div style="margin:0px 8px;">
        <!--tabs-->
        <div style="margin-left: 17px;">
          <div class="themesTab" style="border-top:1px solid #fff !important;background-color:#fff !important;">
            <div class="W31"><button :class="{W100:true,H35:true,tablinks:true,active:dltabs==1}" @click="dltabs=1">最近10期</button></div>
            <div class="W31"><button class="W100 H35 tablinks" @click="dltabs=2">今日全部</button></div>
            <div class="W31"><button class="W100 H35 tablinks" @click="dltabs=3">官網</button></div>
          </div>
        </div>
        <!--tabs index-->
        <div>
          <div id="Par1" :class="{tab_dc:true,ShowMe:dltabs==1,NoShow:dltabs!=1}">
            <!-- 最近10期 -->
            <div class="Game_data_in Game_result">
              <div class="Game_dataView bet_results">
                <!-- 1 result 賽車-->  
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL">733815</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_Pk10">
                        <div class="DW_N car1">1</div>
                        <div class="DW_N car4">4</div>
                        <div class="DW_N car10">10</div>
                        <div class="DW_N car7">7</div>
                        <div class="DW_N car3">3</div>
                        <div class="DW_N car5">5</div>
                        <div class="DW_N car9">9</div>
                        <div class="DW_N car8">8</div>
                        <div class="DW_N car6">6</div>
                        <div class="DW_N car2">2</div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>冠亞和：</span>
                          <span>5</span>
                          <span>小</span>
                          <span>單</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 2 result 時時彩-->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL"> 20190522029</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_ball5 red_ball">3</div>
                        <div class="DW_ball5 red_ball">7</div>
                        <div class="DW_ball5 red_ball">6</div>
                        <div class="DW_ball5 red_ball">6</div>
                        <div class="DW_ball5 red_ball">9</div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>和值：</span>
                          <span>29</span>
                          <span>大</span>
                          <span>單</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 3 result 快樂十分-->
                <!-- 19,20 is red color, others blue -->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL">190522034</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_ball8 blue_ball">16</div>
                        <div class="DW_ball8 blue_ball">13</div>
                        <div class="DW_ball8 blue_ball">10</div>
                        <div class="DW_ball8 blue_ball">07</div>
                        <div class="DW_ball8 blue_ball">11</div>
                        <div class="DW_ball8 red_ball">20</div>
                        <div class="DW_ball8 red_ball">19</div>
                        <div class="DW_ball8 blue_ball">06</div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>和值：</span>
                          <span>102</span>
                          <span>大</span>
                          <span>雙</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 4 result 3D-->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL"> 2019135</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_ball3 red_ball">7</div>
                        <div class="DW_ball3 red_ball">8</div>
                        <div class="DW_ball3 red_ball">9</div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>和值：</span>
                          <span>24</span>
                          <span>大</span>
                          <span>雙</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 5 result Keno20-->
                <!-- 1~40 藍, 41~80 紅 -->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL"> 953531</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_ball10 blue_ball">3</div>
                        <div class="DW_ball10 blue_ball">6</div>
                        <div class="DW_ball10 blue_ball">9</div>
                        <div class="DW_ball10 blue_ball">11</div>
                        <div class="DW_ball10 blue_ball">12</div>
                        <div class="DW_ball10 blue_ball">16</div>
                        <div class="DW_ball10 blue_ball">25</div>
                        <div class="DW_ball10 blue_ball">28</div>
                        <div class="DW_ball10 blue_ball">30</div>
                        <div class="DW_ball10 blue_ball">31</div>
                      </div>
                      <div class="DW_balltable">
                        <div class="DW_ball10 blue_ball">38</div>
                        <div class="DW_ball10 blue_ball">39</div>
                        <div class="DW_ball10 red_ball">48</div>
                        <div class="DW_ball10 red_ball">53</div>
                        <div class="DW_ball10 red_ball">54</div>
                        <div class="DW_ball10 red_ball">59</div>
                        <div class="DW_ball10 red_ball">60</div>
                        <div class="DW_ball10 red_ball">66</div>
                        <div class="DW_ball10 red_ball">69</div>
                        <div class="DW_ball10 red_ball">79</div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>和值：</span>
                          <span>736</span>
                          <span>小</span>
                          <span>雙</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 6 result Mark6 -->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL"> 19056</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/21 21:30:00</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_ball_m6 blue_ball">
                          <div>04</div>
                          <span>猴</span>
                        </div>
                        <div class="DW_ball_m6 red_ball">
                          <div>07</div>
                          <span>蛇</span>
                        </div>
                        <div class="DW_ball_m6 green_ball">
                          <div>21</div>
                          <span>兔</span>
                        </div>
                        <div class="DW_ball_m6 red_ball">
                          <div>35</div>
                          <span>牛</span>
                        </div>
                        <div class="DW_ball_m6 blue_ball">
                          <div>41</div>
                          <span>羊</span>
                        </div>
                        <div class="DW_ball_m6 red_ball">
                          <div>24</div>
                          <span>鼠</span>
                        </div>
                        <!--sp number-->
                        <div class="DW_Special">
                          <div class="DW_ball_m6 red_ball">
                            <div>18</div>
                            <span>馬</span>
                          </div>
                        </div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>總數：</span>
                          <span>150</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
                <!-- 7 快3-->
                <div class="resultWrap">
                  <div class="result_Title">
                    <span class="result_textL"> 20190522025</span><span style="margin-left:1%;">期</span>
                    <span class="result_textR">2019/05/22 17:06:57</span>
                  </div>  
                  <div class="result_contain">
                    <div class="DW_game">
                      <div class="DW_balltable">
                        <div class="DW_sabo3 Num_3"></div>
                        <div class="DW_sabo3 Num_4"></div>
                        <div class="DW_sabo3 Num_4"></div>
                      </div>
                      <div class="grayLine"></div>
                      <div class="DW_text">
                        <div class="gray2_t">
                          <span>點數：</span>
                          <span>11</span>
                          <span>大</span>
                          <span>單</span>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>

              </div><!-- Game_dataView End-->
            </div>
          </div>
          <div id="Par2" :class="{tab_dc:true,ShowMe:dltabs==2,NoShow:dltabs!=2}">
            <!-- 今日全部 -->
          </div>
          <div id="Par3" :class="{tab_dc:true,ShowMe:dltabs==3,NoShow:dltabs!=3}">
            <!-- 官網 -->
          </div>
        </div>
      </div>

    </div>
  </div>
  <!-- DialogEnd-->

</div>
</template>

<script>
import n_tabs from '@/assets/js/tabs.js'

export default {
  name: 'Home',
  data () {
      console.log("hi")
    return {
      active: null,
      text: 'Format Test',
      mytabs:1,
      dltabs:1,
      myodd:true,
      bet_record : [
        {title:'香港六合彩', issue:'20190520125期', billNum:'123456123456', itemBig:'下注大項', itemSmall:'下注小項', betNum:'下注號碼', betOdds:'賠率', result1:'輸贏', result2:'結果',bonusrate:'退水', amount:'投注額'},
        {title:'香港六合彩', issue:'20190520126期', billNum:'123456123457', itemBig:'下注大項', itemSmall:'下注小項', betNum:'04', betOdds:'10', result1:'0', result2:'0',bonusrate:'0', amount:'1000'},
        {title:'香港六合彩', issue:'20190520127期', billNum:'123456123458', itemBig:'下注大項', itemSmall:'下注小項', betNum:'03', betOdds:'10', result1:'0', result2:'0',bonusrate:'0', amount:'1000'},
        {title:'香港六合彩', issue:'20190520128期', billNum:'123456123459', itemBig:'下注大項', itemSmall:'下注小項', betNum:'02', betOdds:'10', result1:'0', result2:'0',bonusrate:'0', amount:'1000'}
      ]
    }
  },
  created() {
  },
  components: {

  },
  methods:{
    backtohome:function(){
      window.location.href = "http://"+location.host
    },
    gotodash:function(){
      this.$router.push({name: 'initData'});
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* width */
@media only screen and (min-width: 1025px) and (max-width: 1366px) {
  .terms-content .themesTab_body {
    width: 90% !important;/*94*/
  }
  .tabBtn {
    min-width: 140px !important;/*82*/
  }
  .tab_dc {
    max-height: 628px !important;
  }
}
@media only screen and (min-width: 925px) and (max-width: 1024px) {
  .terms-content .themesTab_body {
    width: 90% !important;
  }
  .tabBtn {
    min-width: 104px !important;
  }  
  .tab_dc {
    max-height: 445px !important;
  }
}
@media only screen and (min-width: 823px) and (max-width: 924px) {
  .terms-content ol {
    /*height: 762px;*/
    height: 812px;
  }
  .terms-content {
    height: 1250px !important;
  }
  .tabcontent {
    margin-left: 15px;
  }
  .terms-content .themesTab_body {
    width: 88% !important;/*90*/
  }
  .tabBtn {
    min-width: 100px !important;/*81*/
  }
}
@media only screen and (min-width: 769px) and (max-width: 822px){
  .terms-content .themesTab_body {
    width: 88% !important;/*95*/
  }
  .tabBtn {
    min-width: 98px !important;
  }    
}
@media only screen and (min-width: 700px) and (max-width: 768px){
  .terms-content ol {
    /*height: 506px;*/
    height: 556px;
  }
  .tabcontent {
    margin-left: 22px;
  }
  .terms-content .themesTab_body {
    width: 89% !important;
  }
  .tabBtn {
    min-width: 85px !important;
  }  
}
@media only screen and (min-width: 640px) and (max-width: 667px){
  .terms-content .themesTab_body {
    width: 88% !important; /*94%*/
  }
  .tabBtn {
    min-width: 80px !important;
  }    
}
@media only screen and (min-width: 568px) and (max-width: 639px){
  .terms-content .themesTab_body {
    width: 86% !important;/*92*/
  }
}
@media only screen and (min-width: 400px) and (max-width: 402px){
  .terms-content .themesTab_body {
    width: 87% !important;
  }
}

/* height*/
@media only screen and (min-height: 1025px) and (max-height: 1366px){
  .zxDiv {
    height: 1250px !important;
  }
  .terms-content .themesTab_body {
    width: 90% !important;
  }
  .tabBtn {
    min-width: 102px !important;
  }  
  .tab_dc {
    max-height: 930px !important;
  }
}
@media only screen and (min-height: 1000px) and (max-height: 1024px) and (max-width: 768px){
  .zxDiv {
    height: 1250px !important;
  }
  .tab_dc {
    max-height: 670px !important;
  }    
}
@media only screen and (min-height: 813px) and (max-height: 823px){
  .terms-content ol {
    /*height: 506px;*/
    height: 556px;
  }
  .tabBtn {
    min-width: 57px !important;
  }
  .tab_dc {
    max-height: 535px !important;
  }  
}
@media only screen and (min-height: 800px) and (max-height: 812px){
  .terms-content ol {
    /*height: 506px;*/
    height: 556px;
  }
  .tabBtn {
    min-width: 52px !important;
  }
  .tab_dc {
    max-height: 525px !important;
  }
}
@media only screen and (min-height: 737px) and (max-height: 767px){
  .terms-content ol {
    /*height: 506px;*/
    height: 556px;
  }
  .tabBtn {
    min-width: 57px !important;
  }
  .tab_dc {
    max-height: 466px !important;
  }
}
@media only screen and (min-height: 668px) and (max-height: 736px){
  .terms-content .themesTab_body {
    width: 88% !important;
  }  
  .terms-content ol {
    /*height: 468px;*/
    height: 518px;
  }
  .tabBtn {
    min-width: 60px !important;
  }
  .tab_dc {
    max-height: 466px !important;
  }
}
@media only screen and (min-height: 641px) and (max-height: 667px){
  .terms-content ol {
    /*height: 372px;*/
    height: 422px;
  }
  .tab_dc {
    max-height: 412px !important;
  }
}
@media only screen and (min-height: 569px) and (max-height: 640px){
  .tab_dc {
    max-height: 390px !important;
  }
}
@media only screen and (min-height: 421px) and (max-height: 568px){
  .tab_dc {
    max-height: 330px !important;
  }
}
@media only screen and (min-height: 410px) and (max-height: 420px){
  .tab_dc {
    max-height: 180px !important;
  }
}
@media only screen and (min-height: 375px) and (max-height: 400px){
  .terms-content ol {
    /*height: 300px;*/
    height: 350px;
  }
  .OpenPrize_pk10 {
    width: 19px !important;
  }
  .tab_dc {
    max-height: 155px !important;
  }
}
@media only screen and (min-height: 321px) and (max-height: 374px){
  .terms-content ol {
    /*height: 300px;*/
    height: 350px;
  }
  .OpenPrize_pk10 {
    width: 19px !important;
  }
  .tabBtn {
    min-width: 77px !important;/*45*/
  }
  .tab_dc {
    max-height: 142px !important;
  }
}
@media only screen and (min-height: 0px) and (max-height: 320px){
  .terms-content ol {
    /*height: 300px;*/
    height: 350px;
  }
  .OpenPrize_pk10 {
    width: 19px !important;
  }
  .tabBtn {
    min-width: 80px !important;/*45*/
  }
  .tab_dc {
    max-height: 116px !important;
  }
}


/*-------------*/
/* Theme Style */
/*-------------*/
.theme1 .header {
    color: #fff;
    border-bottom: 1px solid #6086a2;
    background-image: linear-gradient(#437dde, #222a38);
}
.theme1 .themeBtn {
    background-image: linear-gradient(#437dde, #222a38);
}
.theme1 .zxDiv {
    background-color: #d8d2d2;
}
.theme1 .themesBg {
    width: 100%;
    background-color: #595959;
    height: 34px;
    position: fixed;
    top: 109px;
}
.theme1 .themesHead {
    background-color: #595959;
    /*border-right: 1px solid;*/
}
.theme1 .themesTab_body {
    position: fixed;
    margin-top: -7px;
    margin-left: -1px;
    z-index: 10;
    width: 86%;
    line-height: 10px;
    background-color: #f1f1f1;
    border-left: 1px solid;
    /*border-right: 1px solid;*/
    border-bottom: 1px solid #dadada;
}
.theme1 .themesTab {
  display: -webkit-box;
  overflow-y: hidden;
  overflow-x: auto;
  color: #827e7e;  
  border-top: 1px solid #ccc;
  background-color: #f1f1f1;
}
.theme1 .themesTab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 10px 10px;
  transition: 0.3s;
  font-size: 0.9rem;
}
.theme1 .themesTab button:hover {
  color: #000000;  
  border-bottom: 3px solid #656565;
}
.theme1 .themesTab button.active {
  color: #000000;  
  border-bottom: 3px solid #656565;
}
.theme1 .numberList {
    padding: 0;
    margin: 0;
    list-style: none;
    display: block;
    margin-block-start: 1em;
    margin-block-end: 1em;
    margin-inline-start: 0px;
    margin-inline-end: 0px;
    padding-inline-start: 10px;
}
.theme1 .numberList li {
  margin: .6% .6% .6% 0.8%;
  width: 18%;
  white-space: pre-line;
  font-size: 0.75rem;
  float: left;  
}
.theme1 .numberList li a {
    display: block;
    padding: 12px 0 6px 0;
    border-radius: .5em;
    /*border: 1px solid #eee;*/
    border: 1px solid #1976d2;
    /*font-size: 1.2em;*/
    font-size: 1em;
    font-weight: 500;
    line-height: 1;
    text-align: center;
    text-decoration: none;
    transition: all .5s; 
    color: #333;
    background-color: #eff7ff;
    cursor: pointer;
}
.theme1 .numberList small {
    font-size: 0.6rem;
    color: red;
}
.theme1 .numberList li.active a{
    background-color: #ff0!important;
}
.theme1 .Game_menu_title {
  background-image: linear-gradient(#3873d6, #578eec);
}
.theme1 .titleDialog {
  font-size: small;
  color: #fff600;
}
.theme1 .titleSpan {
  color: #ffffff;
}

/*-----------*/
/*   Begin   */
/*-----------*/

/* Head Part */
.header {
    margin-left: -1px;
    position: fixed;
    width: 100%;
    top: 0;
    z-index: 99;
}
.header_top {
    height: 50px;
    text-align: center;
    position: relative;
}
.header_title {
    font-size: 1.6em;
    position: absolute;
    line-height: 45px;
    margin: 0px auto;
    left: 0;
    right: 0;
    width: 47%;
}

/* Header_btnLeft Css */
.header_btnLeft {
    position: absolute;
    margin: auto 0px;
    left: 0;
    top: 0;
    bottom: 0;
    height: 100%;
}
.btn_home {
    background: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fbtn_home.png?alt=media&token=1a3397c6-c4be-4337-a6ae-677b486b9369) no-repeat center;
    background-size: 55% auto;
    height: 48px !important;
}
.btn_lotteryResult {
    background: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fbtn_lotteryResult.png?alt=media&token=22e29efe-4702-46f8-bcf6-1d7241bc1027) no-repeat center;
    background-size: 59% auto;
    height: 50px !important;
}
.btn_home, .btn_lotteryResult, .btn_betRecord, .btn_menu {
    cursor: pointer;
    height: 100%;
    width: 45px; 
    float: left;
    opacity: 0.5;    
}

/* Header_btnRight Css */
.header_btnRight {
    position: absolute;
    margin: auto 0px;
    right: 0;
    top: 0px;
    bottom: 0;
    height: 100%;
}
.btn_betRecord {
    background: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fbtn_betRecord.png?alt=media&token=d3b91444-ed6c-43d8-b82f-acb6f750a417) no-repeat center;
    background-size: 48% auto;
    height: 48px !important;
}
.btn_menu {
    background: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fbtn_menu.png?alt=media&token=27adff13-a699-469a-a0a7-34a2b3533010) no-repeat center;
    background-size: auto 42%;
    height: 48px !important;
}
.headerPage_down {
    font-size: 0.9em;
    width: 100%;
    padding: 0 3%;
    table-layout: auto;
}
.headerPage_down {
    display: table;
    width: 100%;
    text-align: center;
    height: 32px;
    line-height: 32px;
    background-color: #000;
    border-bottom: 1px solid #454545;
    box-sizing: border-box;
    table-layout: fixed;
    font-size: 1.2em;
    /*table-layout: auto;*/
    /*padding: 0px 3%;*/
}
.header_phase {
    display: table-cell;
    color: #fff;
    vertical-align: middle;
    text-align: left;
    white-space: nowrap;
    /*width: 35%;*/
}
.header_phaseNum {
    color: #ff7d7d;
    margin-right: 3px;
}
.header_time {
    display: table-cell;
    vertical-align: middle;
    color: #f00;
    font-size: 1em;
    text-align: center;
    /*width: 30%;*/
    padding-right: 3%;
}
.greensp {
    color: #369c57;
}
.header_money {
    display: table-cell;
    font-size: 1em;
    color: #ffe400;
    background: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Ficon_credit.png?alt=media&token=07db7947-cdfc-4412-9a3e-182ec22c58d4) no-repeat 8% 50%;
    background-size: auto 56%;
    vertical-align: middle;
    padding-left: 10%;
    white-space: nowrap;
}

/* Pre Result */
.Prev_result {
    position: fixed;
    z-index: 10;
    width: 100%;    
}
.Div_result {
    margin-left: -1px;
    width: 100%;
    top: 28px;
    background-color: rgb(255, 255, 255);
    color: #fff;
    text-align: center;
    font-size: 1.0em;
    line-height: 25px;
    position: relative;
    cursor: pointer;
}
.control_L {
    text-align: center;
    width: 25%;
    float: left;
    color: #615c5c;
    font-size: 1.2em;
    font-weight: bold;
}
.control_L2 {
    margin-left: 3px;
    font-size: 0.8em;
}
.control_R {
    display: table;
    margin: 0 auto;
}

/* PK10 OpenPrize */
.OpenPrize_pk10 {
    width: 21px;
    line-height: 21px !important;
    float: left;
    color: #fff;
    border-radius: 10%;
    margin: 2px !important;
    font-size: 1.2em !important;
    font-weight: bold;
}
.car1 {
   background-color: #ffc000; 
}
.car2 {
   background-color: #01c0ff;
}
.car3 {
   background-color: #4B4B4B;
}
.car4 {
   background-color: #ff6d00;
}
.car5 {
   background-color: #2fe1bd;
}
.car6 {
   background-color: #3d009b;
}
.car7 {
   background-color: #b6b6b6;
}
.car8 {
   background-color: #fe0000;
}
.car9 {
   background-color: #582524;
}
.car10 {
   background-color: #006a39;
}

/*  Hr Line */
.Hrline-botton {
    border-right: 1px solid #9a9a9a;
    border-left: 1px solid #9a9a9a;
    border-bottom: 1px solid #9a9a9a;    
}
.Hrline-top {
    border-bottom: 1px solid #9a9a9a;    
}

/* Div Content */
.zxDiv {
    display: block;
    padding-top: 60px;
    height: 902px;
    text-align: center;
}
.v-tabs, .v-tabs__bar {
    position: fixed;
    width: 100%;
    border-radius: inherit;
    border-bottom: 1px solid;
    border-bottom-color: #ccc3c3 !important;
    border-right: 2px solid;
    border-right-color: #000000 !important;
    background-color: #656565!important;
    border-color: #656565!important;
}

/* Btn Css */
.btnChoose {
    margin-right: 20px;
}
.btnNum {
    margin-right: 3px;
    margin-left: 3px;
    color: #ffe500
}
.btnSub {
    color: #ffe500
}

/* body content */
.terms-content {
    padding: 0px;
    height: 902px;
    margin-top: 55px;
    background-color: #f3f3f3;
    border: 1px solid #50678b;
    /* border-radius: 8px; */
    font-size: 12px !important;
}
.terms-content h3, hr, p {
  margin-bottom: 10px !important;
}
.terms-content ol {
  padding-left: 20px !important;
  overflow: scroll;
  /* height: 300px; */
}
.terms-content .list-styled {
  margin-bottom: 20px;
}
.terms-content li {
  margin-bottom: 8px;
}.terms-content .color-focus {
  color: #c50000;
}
.terms-content .text-center {
  text-align: center;
}
.terms-content .pointer {
  /* cursor: pointer; */
  border-radius: 3px;
  color: #fff;
  background-image: linear-gradient(#ffa200, #ff9800);
}
.terms-content .le {
  height: 54px;
  line-height: 52px;
  border-radius: 4px;
  color: #fff;
  background-image: linear-gradient(#7c7d7d, #7c7d7d);
}
.terms-content .cv {
  height: 54px;
  line-height: 52px;
  border-radius: 4px;
  color: #fff;
  /*background-image: linear-gradient(#437dde, #222a38);*/
}


/*-------------*/
/* Foot Button */
/*-------------*/
.foot_Bet {
    position: fixed;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 67px;
    background-color: #f3f3f3;
    border: 1px solid #9a9a9a;
    z-index: 10;
    display: table;
}
.foot_Btn {
    position: relative;
    /*padding: 0px 3%;*/
    text-align: center;  
}


/*---------------*/
/*    Dialog     */
/*---------------*/
.maskAll {
    display: none;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.46);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 999;
    overflow-y: auto;  
}
.maskAll_result {
    display: block;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.46);
    position: fixed;
    top: 0;
    left: 0;
    z-index: 999;
    overflow-y: auto;  
}
.Game_menu {
    background-color: #fff;
    position: absolute;
    top: 8% !important;
    left: 0;
    right: 0;
    margin: 0 auto;
    width: 90% !important;
    font-size: 1em;
    height: 82vh;
    border-radius: 8px;
    padding: 0px 5px;
    z-index: 99;
}
.Game_menu_title {
    text-align: center;
    font-weight: bold;
    font-size: medium;    
    height: 40px;
    line-height: 40px;
    color: #fff;
    /*background-color: #539c92;*/
    margin: 0 -5px;
    border-radius: 8px 8px 0 0;
}
.Game_menu-close {
    position: absolute;
    top: 0;
    right: 0px;
    width: 38px;
    height: 38px;
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Ficon_close.png?alt=media&token=d57630e3-b43a-41db-8e3d-7c1c08484633);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 20px 20px;
    cursor: pointer;
    opacity: 0.5;
}
.Game_menu-reset {
    position: absolute;
    top: 0;
    left: 0px;
    width: 38px;
    height: 38px;
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fbtn_LRrefresh.png?alt=media&token=51a11780-68fd-4092-b0aa-ab49ebdf1f75);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 22px 22px;
    cursor: pointer;
    opacity: 0.5;
}
.bet_record {
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0px;
    padding: 2% 2.5%;
    border-radius: 0 0 7px 7px;
    background-color: #262626;
    opacity: 0.8;
}
.betWrapL {
    padding: 1.5% 0;
    width: 49.5%;
    float: left;
    font-size: larger;
}
.betWrapL.borderR {
    border-left: 1px solid #5e5e5e;
    padding-left: 2% !important;  
}
.white_t {
    color: #fff;
}
.yellow_t {
    color: #fff600;
}
.green_t {
    color: #40b401;
}
.red_t {
    color: #f44336;
}
.black_t {
    color: #000000;
}
.gray_t {
    color: #979797;
}
.gray2_t {
    color: #6a6565;
}
.blue_t {
    color: #2e91ff;
}
.tab_dc {
    display: none;
    margin-top: 10px;
    max-height: 388px;
    overflow: auto;
    -webkit-animation: fadeEffect 1s;
    animation: fadeEffect 1s;
    cursor: pointer;
}
.maskAll .v-expansion-panel__header {
    padding: 0px 4px !important;
    min-height: 24px !important;
}
.Lottery_periods {
    font-size: 0.9rem;
    /*color: #fff;*/
    margin-left: 15%;
}
.rl_list {
    padding: 0px !important;
    background-color: #e6e6e6 !important;
    border-radius: 2% 2% 0 0;
}
.rl_listD1 {
    border-radius: 2%;
    margin-top: 8px;
    border-bottom: 6px solid #d2d4d5;
}
.rl_listD2 {
    /*background-color: #e6e6e6;*/
    border-radius: 2%;
    margin-top: 8px;
    border-bottom: 7px solid #d2d4d5;
}
.rl_listP {
    /*padding: 2px 6px!important;*/
    margin-left: -12px;
}
.rl_glay_Line {
    width: 100%;
    height: 1px;
    background-color: #cccccc;
}
.rl_listFoot {
    /*background-color: #e6e6e6;*/
    position: relative;
    display: table;
    width: 100%;
    /*border-bottom-left-radius:5px;*/
    /*border-bottom-right-radius:5px;*/
    /*padding-bottom: 5px;*/
}
.rl_listFoot_H {
    padding: 3px 0;
}
.rl_listFoot_R {
    /*font-size: 1.1em;*/
    float: right;
    width: 45%;
}
.rl_listFoot_L {
    /*font-size: 1.1em;*/
    float: left;
}
.rl_listFoot_xd {
    background-color: #fff;
    border-radius: 5px;  
}


/*---------------*/
/* Dialog-Result */
/*---------------*/
.Game_data_in {
  position: relative;
  text-align: center;
  background-color: #fff;
  border-radius: 0 0 8px 8px;
  margin: 0 -5px;
}
.Game_data_in.Game_result {
  padding: 2% 0 2%;
  height: 100%;
}
.Game_dataView {
  border-bottom: 1px solid #d9d9d9;
  border-top: 1px solid #d9d9d9;
  text-align: left;
}
.Game_dataView.bet_results {
  border-bottom: 0;
  border-top: 0;
  padding: 0;
  max-height: none;
  height: inherit;
  overflow: hidden;
  overflow-Y: auto;
}
.resultWrap {
  width: 94%;
  border-radius: 5px;
  overflow: hidden;
  border: 1px solid #cdcdcd;
  margin: 0 auto 2%;
}
.result_Title {
  font-size: 1.1em; /*0.9*/
  line-height: 2.3em;
  background-color: #e5e5e5;
  border-bottom: 1px solid #cdcdcd;
}
.result_textL {
  float: left;
  padding-left: 3%;
  color: #000;
}
.result_textR {
  float: right;
  padding-right: 3%;
  color: rgba(0,0,0,0.5);
  font-size: 0.9em; /*0.8*/
}
.DW_game {
  /*上下填空*/
  padding: 2% 0 2%;
}
.DW_Pk10 {
  /*賽車類*/
  width: 100%;
  text-align: center;
  margin-bottom: 2%;
}
.DW_balltable {
  /*彩球類*/
  width: 100%;
  text-align: center;
  margin-bottom: 2%;
}
.grayLine {
  width: 100%;
  height: 1px;
  background-color: #cdcdcd;
}
.DW_text {
  margin: 2% 0 0 2%;
  text-align: left;
  font-size: 0.85em; /*0.75*/
  display: table;
  width: 100%;
}
.DW_N {
  margin: 0px 1px;
  width: 20px;
  height: 20px;
  line-height: 20px;
  border-radius: 10%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1.2em;
  font-weight: bold;
}
.DW_ball3 {
  margin: 0px 6px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  border-radius: 50%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1.1em;
 }
.DW_sabo3 {
    margin: 0px 6px;
    width: 30px;
    height: 30px;
    line-height: 30px;
    position: relative;
    display: inline-block;
 }
.DW_ball5 {
  margin: 0px 3px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  border-radius: 50%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1.1em;
 }
.DW_ball8 {
  margin: 0;
  width: 28px;
  height: 28px;
  line-height: 28px;
  border-radius: 50%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1.1em;
 }
.DW_ball10 {
  margin: 0;
  width: 22px;
  height: 22px;
  line-height: 22px;
  border-radius: 50%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1em;
 }
.DW_ball_m6 {
  margin: 0 1px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  border-radius: 50%;
  color: #fff;
  text-align: center;
  position: relative;
  display: inline-block;
  font-size: 1.1em;
 }
.DW_ball_m6 span {
  color: #6a6565;
  font-size: 0.75em; /*0.7*/
}
.DW_Special {
  margin-left: 1px;
  height: 100%;
  padding-left: 5px;
  display: inline-block;
  border-left: 1px solid #cdcdcd;
}

/* Sabo images*/
.Num_1 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum01.png?alt=media&token=6701b31c-1f4e-4795-acf5-72e4c1febcad);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}
.Num_2 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum02.png?alt=media&token=57136695-8772-4186-a4b9-13aa68e560b5);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}
.Num_3 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum03.png?alt=media&token=bd99c9f7-3853-4878-8492-92568e389a31);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}
.Num_4 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum04.png?alt=media&token=0fc63f93-77a1-4904-82ed-4cdcb5970fad);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}
.Num_5 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum05.png?alt=media&token=cd4302c3-cdc8-4ea4-9e64-2c84f7210c03);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}
.Num_6 {
    background-image: url(https://firebasestorage.googleapis.com/v0/b/union-compare.appspot.com/o/demo%2Fnum06.png?alt=media&token=e1783d15-4add-40a1-8474-369ae2ca55ab);
    background-repeat: no-repeat;
    background-position: center;
    background-size: 30px 30px;
}

/*---------------*/
/*  Ball Bgcolor */
/*---------------*/
.red_ball {
   background-color: #c23437; 
}
.blue_ball {
   background-color: #1c76b3; 
}
.green_ball {
   background-color: #369c57; 
}

/*---------------*/
/*   Tabs Css    */
/* Style the tab */
/*
.tab {
  color: #827e7e;  
  overflow-y: hidden;
  overflow-x: auto;
  border: 1px solid #e2e2e2;
  background-color: #f1f1f1;
}
*/
/* Style the buttons inside the tab */
/*
.tab button {
  background-color: inherit;
  float: left;
  border: none;
  outline: none;
  cursor: pointer;
  padding: 10px 10px;
  transition: 0.3s;
  font-size: 0.9rem;
}
*/
/* Change background color of buttons on hover */
/*
.tab button:hover {
  color: #000000;  
  background-color: #ffffff;
  border-bottom: 3px solid #656565;
}
.tab button.active {
  color: #000000;  
  background-color: #ffffff;
  border-bottom: 3px solid #656565;
}
*/

/* Style the tab content */
.tabcontent {
  display: none;
  /*padding: 6px 12px;*/
  margin-top: 40px;
  -webkit-animation: fadeEffect 1s;
  animation: fadeEffect 1s;
  cursor: pointer;
}
.tabBtn {
    display: block;
    position: fixed;
    padding: 0 8px 0 10px;
    margin: 6px auto !important;
    /*border-radius: 20px;*/
    top: 103px;
    right: 0px;
    min-width: 52px;
    height: 34px;
    line-height: 32px;
    font-size: 0.9em;
    box-sizing: border-box;
    text-align: center;
    white-space: nowrap;
    color: #fff;
    background-color: #595959;
    cursor: pointer;
    z-index: 25;
}
/* Fade in tabs */
@-webkit-keyframes fadeEffect {
  from {opacity: 0;}
  to {opacity: 1;}
}
@keyframes fadeEffect {
  from {opacity: 0;}
  to {opacity: 1;}
}

/* Control emement */
.maskAll .v-card div {
  padding: 0px !important;
}
.H35 {
  height: 35px;
}
.W31 {
  width:31%;
}
.W100 {
  width:100%;
}
.ShowMe {
    display:block;
}
.NoShow {
    display:none;
}
.isStop a {
    background-color: grey!important;
}
</style>
