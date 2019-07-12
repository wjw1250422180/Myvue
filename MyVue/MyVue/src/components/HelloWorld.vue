
<style scoped>
* {
  margin: 0;
  padding: 0;
}
.main {
  display: flex;
  flex-direction: row;
  align-items: center;
  text-align: center;
}
/* .right {
  display: flex;
  flex-direction: column;
  margin-left: -100px;
} */
.connent {
  display: flex;
  flex-direction: column;
  margin: auto;
  width: 90%;
  margin: 0px auto;
}
.first {
  width: 100%;
  margin: auto;
  display: flex;
  flex-direction: row;
  background-color: rgb(75, 73, 73);
}
.logochoose {
  width: 20%;
  margin: 40px auto;
  color: white;
}
.logochoose .child {
  display: none;
}
.logochoose:hover .child {
  display: block;
}
.child {
  width: 50px;
  height: 50px;
}
.imge {
  width: 10%;
  height: 100px;
  margin: 5px auto;
}
.maintitle {
  color: white;
  width: 50%;
  margin: auto;
}
.second {
  background-color: rgb(236, 231, 225);
  height: 160px;
  width: 100%;
  margin: 0px auto;
}
.title {
  text-align: center;
  margin-top: 50px;
  color: rgb(110, 28, 28);
}
.imge2 {
  width: 600px;
  height: 60px;
  margin-left: 370px;
  margin-top: 15px;
  margin-bottom: 40px;
}
.input {
  width: 70%;
  margin: 10px auto;
  /* margin-left: 350px;
  margin-top: 15px;
  margin-bottom: 40px; */
}
.Input {
  width: 60%;
  height: 43px;
  border: 1.3px solid rgb(110, 28, 28);
}
.serch {
  height: 43px;
  width: 10%;
  margin: auto;
  border: 2px solid rgb(110, 28, 28);
  background-color: rgb(110, 28, 28);
  color: aliceblue;
}
.third {
  display: flex;
  flex-direction: column;
  /* margin-left: 10px;
  margin-top: 30px; */
  margin: 0px auto;
  width: 100%;
  background-color: gainsboro;
}
.One {
  display: flex;
  flex-direction: row;
  width: 100%;
  margin: 10px auto;
}
.one {
  display: flex;
  flex-direction: column;
  width: 80%;
  margin: auto;
}
.colum1 {
  display: flex;
  flex-direction: row;
  margin-left: 40px;
  margin-top: 20px;
}
.local {
  margin-left: 10px;
}
.serchinput {
  height: 30px;
  width: 30px;
  margin-left: 5px;
}
.serchinput1 {
  height: 30px;
  width: 30px;
  margin-left: 5px;
  margin: -1px;
}

.label {
  font-size: 12px;
  margin-left: 10px;
}
.sercher {
  width: 100px;
  height: 40px;
  margin-left: 100px;
  margin-top: 50px;
  background-color: rgb(110, 28, 28);
  color: aliceblue;
}
.txt {
  margin-top: 90px;
  margin-left: -120px;
  color: rgb(30, 117, 151);
  width: 110px;
  height: 40px;
}
.three {
  text-align: center;
  width: 100%;
  margin: 0 auto;
}
.four {
  text-align: center;
  background-color: rgb(117, 117, 117);
  height: 40px;
}

.smallbtn {
  background-color: rgb(0, 183, 255);
  margin-top: -50px;
  margin-left: -17px;
}
.smallbtn1 {
  background-color: rgb(0, 183, 255);
  margin-top: -10px;
  margin-left: -10px;
}
.smallbtn2 {
  background-color: rgb(0, 183, 255);
  margin-top: 40px;
  margin-left: -16px;
}
/* .toTop {
  background-color: black;
}
.toptxt {
  background-color: black;
} */
</style>

<template>
  <layout>
    <header>
      <div class="main">
        <div class="connent">
          <div class="first">
            <img src="../image/1.png" class="imge" />
            <h1 class="maintitle">小巨靓号</h1>
            <!-- <div class="main-top-right" @mouseenter="enter2wm()" @mouseleave="out2wm()"> -->
            <div class="logochoose">
              手机选号
              <img class="child" src="../image/h5.png" />
            </div>
            <!-- <Tooltip class="logochoose" max-width="200" content="这是一张二维码图片">手机选号</Tooltip> -->
          </div>

          <div class="second">
            <h1 class="title">号码交易，尽在小巨</h1>
            <div class="input" id="input">
              <input name id placeholder="请输入要搜索的内容" v-model="searchText" class="Input" />
              <button type="button" class="serch">搜索</button>
            </div>
          </div>

          <div class="third">
            <div class="One">
              <div class="one">
                <div class="colum1">
                  <h3 :style="{margin: '6px 10px 0px '}">运营商：</h3>
                  <Select v-model="model1" style="width:100px">
                    <Option
                      v-for="item in cityList1"
                      :key="item.value2"
                      value="value2"
                    >{{ item.label }}</Option>
                  </Select>
                  <h3 :style="{margin: '6px 20px 0px '}">归属地：</h3>
                  <Select v-model="model2" style="width:100px">
                    <Option
                      v-for="item in cityList2"
                      :key="item.value3"
                      value="value3"
                    >{{ item.label }}</Option>
                  </Select>

                  <Select v-model="model3" style="width:100px " class="local">
                    <Option
                      v-for="item in cityList3"
                      :key="item.value4"
                      value="value4"
                    >{{ item.label }}</Option>
                  </Select>
                  <h3 :style="{margin: '6px 20px 0px '}">号码规律：</h3>
                  <Select v-model="model4" style="width:100px">
                    <Option
                      v-for="item in cityList4"
                      :key="item.value5"
                      value="value5"
                    >{{ item.label }}</Option>
                  </Select>
                  <h3 :style="{margin: '6px 20px 0px '}">价格区间：</h3>
                  <Input v-model="max" style="width: 60px" />
                  <h3 :style="{margin: '7px '}">~</h3>
                  <Input v-model="min" style="width: 60px" />
                </div>
                <div class="colum1">
                  <h3 :style="{margin: '6px 10px 0px '}">精准搜索：</h3>
                  <Tooltip
                    max-width="200"
                    content="说明
                  1、支持输入后自动切换下一格，

                  2、退格删除，在退格返回上一格"
                  >
                    <Button shape="circle" icon="md-menu" class="smallbtn1"></Button>
                  </Tooltip>
                  <Input disabled value="1" class="serchinput1" />
                  <input
                    :maxlength="1"
                    v-for="(item,index) in inputList"
                    :key="item.val1"
                    type="text"
                    v-model="item.val"
                    id="1"
                    class="serchinput"
                    @keyup="nextFocus($event,index) "
                    autofocus
                  />
                  <!-- <body > 
                  <form>
                <input maxlength="1" class="serchinput" type="text" v-on:input = "movenext(0)"@keydown="deletvalue($event,index)">
                <input maxlength="1" class="serchinput" type="text" v-on:input = "movenext(1)">
                <input maxlength="1" class="serchinput" type="text" v-on:input = "movenext(2)">
                <input maxlength="1" class="serchinput" type="text" v-on:input = "movenext(3)">
                  </form>
                  </body>-->

                  <!-- <Input :maxlength="1" type='text' id='1' class="serchinput" autofocus  @onfocus='getforcus(1)' v-on:input='getNextObj(1)'/>
                <Input :maxlength="1" type='text' id='2'   class="serchinput" autofocus @onfocus='getforcus(2)' v-on:input='getNextObj(2)' />
                <Input :maxlength="1" type='text' id='3'  class="serchinput1" autofocus @onfocus='getforcus(3)' v-on:input='getNextObj(3)' />
                <Input :maxlength="1" type='text' id='4' class="serchinput" autofocus  @onfocus='getforcus(4)' v-on:input='getNextObj(4)'/>
                <Input :maxlength="1" type='text' id='5'  class="serchinput" autofocus @onfocus='getforcus(5)' v-on:input='getNextObj(5)'/>
                <Input :maxlength="1" type='text' id='6' class="serchinput" autofocus  @onfocus='getforcus(6)' v-on:input='getNextObj(6)'/>
                <Input :maxlength="1" type='text' id='7'  class="serchinput1" autofocus @onfocus='getforcus(7)' v-on:input='getNextObj(7)'/>
                <Input :maxlength="1" type='text' id='8'   class="serchinput" autofocus  @onfocus='getforcus(8)' v-on:input='getNextObj(8)'/>
                <Input :maxlength="1" type='text' id='9'  class="serchinput" autofocus  @onfocus='getforcus(9)' v-on:input='getNextObj(9)'/>
                  <Input :maxlength="1" type='text' id='10'  class="serchinput" autofocus  @onfocus='getforcus(10)' v-on:input='getNextObj(10)'/>-->
                  <h3 :style="{margin: '6px 20px 0px '}">排列方式：</h3>
                  <Select v-model="model5" style="width:130px">
                    <Option
                      v-for="item in cityList5"
                      :key="item.value6"
                      value="value6"
                    >{{ item.label }}</Option>
                  </Select>
                </div>
                <div class="colum1">
                  <label class="label">
                    <input type="checkbox" v-model="gender" />
                    不带0
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender1" />
                    不带1
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender2" />
                    不带2
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender3" />
                    不带3
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender4" />
                    不带4
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender5" />
                    不带5
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender6" />
                    不带6
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender7" />
                    不带7
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender8" />
                    不带8
                  </label>
                  <label class="label">
                    <input type="checkbox" v-model="gender9" />
                    风水号
                  </label>
                </div>
              </div>
              <button type="button" class="sercher">筛选号码</button>
              <Tooltip
                max-width="200"
                content="说明

                  1、对已搜索的号码进行更多的筛选；

                 2、若精准搜索有填写时，则上方的模糊搜索清空不带条件搜索，只搜索精准搜索；"
              >
                <Button shape="circle" icon="md-menu" class="smallbtn2"></Button>
              </Tooltip>
              <Button type="text" class="txt" @click="empty">重置搜索条件</Button>
            </div>
            <div class="two">
              <Table stripe :columns="columns1" :data="data1"></Table>
            </div>
            <div class="three">
              <Page :total="100" show-elevator />
            </div>
            <div class="four">
              <div>闽ICP备13012512号-1</div>
              <div>Copyright 2010-2019 小巨靓号 -小巨网络科技有限公司 版权所有</div>
            </div>
          </div>
        </div>
        <!-- <div class="right">
          <div class="toTop" v-if="isToTop" @click="toTop">
            <img class="topimg" src="../image/top.png" />
            <div class="toptxt">TOP</div>
          </div>
        </div>-->
      </div>
    </header>
  </layout>
</template>
<script src="https://cdn.jsdelivr.net/npm/vue"></script>
<script>
export default {
  data() {
    return {
      inputList: [
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' },
        { val: '' }
      ],
      searchText: '', // 搜索框输入数据
      model1: '',
      model2: '',
      model3: '',
      model4: '',
      model5: '',
      max: '',
      min: '',
      gender: '',
      gender1: '',
      gender2: '',
      gender3: '',
      gender4: '',
      gender5: '',
      gender6: '',
      gender7: '',
      gender8: '',
      gender9: '',

      cityList1: [
        '不限',
        {
          value2: '中国电信',
          label: '中国电信'
        },
        {
          value2: '中国联通',
          label: '中国联通'
        },
        {
          value2: '中国移动',
          label: '中国移动'
        },
        {
          value2: '虚商',
          label: '虚商'
        }
      ],

      cityList2: [
        '不限',
        {
          value3: '北京',
          label: '北京'
        },
        {
          value3: '福建',
          label: '福建'
        },
        {
          value3: '上海',
          label: '上海'
        },
        {
          value3: '河北',
          label: '河北'
        },
        {
          value3: '河南',
          label: '河南'
        }
      ],
      cityList3: [
        '不限',
        {
          value4: 'New York',
          label: 'New York'
        },
        {
          value4: 'London',
          label: 'London'
        },
        {
          value4: 'Sydney',
          label: 'Sydney'
        },
        {
          value4: 'Ottawa',
          label: 'Ottawa'
        },
        {
          value4: 'Paris',
          label: 'Paris'
        },
        {
          value4: 'Canberra',
          label: 'Canberra'
        }
      ],

      cityList4: [
        {
          value5: '尾号AABB',
          label: '尾号AABB'
        },
        {
          value5: '尾号AAAB',
          label: '尾号AAAB'
        },
        {
          value5: '尾号ABBB',
          label: '尾号ABBB'
        },
        {
          value5: '尾号ABAB',
          label: '尾号ABAB'
        }
      ],
      cityList5: [
        {
          value6: '价格从高到低',
          label: '价格从高到低'
        },
        {
          value6: '价格从低到高',
          label: '价格从低到高'
        },
        {
          value6: '用户综合评价',
          label: '用户综合评价'
        }
      ],
      columns1: [
        {
          title: '手机号码',
          key: 'num'
        },
        {
          title: '归属地',
          key: 'place'
        },
        {
          title: '运营商',
          key: 'person'
        },
        {
          title: '售价',
          key: 'price'
        }
      ],
      data1: [
        {
          num: '15260499012',
          place: '福建泉州',
          person: '移动',
          price: '￥1999'
        },
        {
          num: '15265456398',
          place: '福建福州',
          person: '电信',
          price: '￥1929'
        },
        {
          num: '15981854625',
          place: '福建漳州',
          person: '联通',
          price: '￥999'
        },
        {
          num: '15698548565',
          place: '福建福州',
          person: '移动',
          price: '￥1999'
        },
        {
          num: '15698548565',
          place: '福建厦门',
          person: '电信',
          price: '￥1859'
        },
        {
          num: '15698548565',
          place: '福建福州',
          person: '移动',
          price: '￥1299'
        },
        {
          num: '15698548565',
          place: '福建福州',
          person: '移动',
          price: '￥1487'
        },
        {
          num: '15698548565',
          place: '福建福州',
          person: '移动',
          price: '￥2149'
        },
        {
          num: '15698548565',
          place: '福建福州',
          person: '移动',
          price: '￥1149'
        }
      ]
    }
  },

  methods: {
    // movenext(index){
    //   var value=decument.forms[0].elements[index].value;
    //   var limit=decument.forms[0].length-1;
    //   if(limit  === index){
    //     return;
    //   }
    //   if(value.length === 1){
    //     document.forms[0].elements[index+1].focus();
    //   }
    // },
    // getfouces(id){
    //   document.getElementById(id).select();
    // },
    // getNextObj(id){
    //   var obj=document.getElementById(id);
    //   if(obj.value.toString().length == 1){
    //     document.getElementById(id).blur();
    //     var nextid=id+1;
    //     document.getElementById(nextid).focus;
    //   }
    // },
    enter2wm() {
      document.getElementById('2wm').style.height = '120px'
    },
    out2wm() {
      document.getElementById('2wm').style.height = '0px'
    },
    empty() {
      this.searchText = ''
      this.model1 = ''
      this.model2 = ''
      this.model3 = ''
      this.model4 = ''
      this.model5 = ''
      this.max = ''
      this.min = ''
      this.gender = ''
      this.gender1 = ''
      this.gender2 = ''
      this.gender3 = ''
      this.gender4 = ''
      this.gender5 = ''
      this.gender6 = ''
      this.gender7 = ''
      this.gender8 = ''
      this.gender9 = ''
      for (var i = 0; i < 10; i++) {
        this.inputList[i].val = ''
      }
    },

    nextFocus(el, index) {
      var dom = document.getElementsByClassName('serchinput') //获取class名称
      var currInput = dom[index] //当前input位置
      var lastInput = dom[index - 1] //前面一个input位置
      var nextInput = dom[index + 1] //后面一个input位置
      /*这里的keyCode=8是backspaces向前删除键*/

      if (el.keyCode != 38) {
        if (el.keyCode != 8) {
          if (!isNaN(el.target.value)) {
            if (index < this.inputList.length - 1) {
              //若写index != this.inputList.length ),则最后一个输入框会报错
              nextInput.focus()
            }
          } else {
            alert('请输入数字')
            this.inputList[index].val = ''
          }
        } else {
          if (index != 0) {
            //要判断当前（最后）输入框，否则会报错
            lastInput.focus()
          }
        }
      } else {
        //按下左键向前面的input聚焦
        if (index != 0) {
          //要判断当前（最后）输入框，否则会报错
          lastInput.focus()
        }
      }
      if (el.keyCode == 37) {
        lastInput.focus()
      }
    }
  }
}
</script>
