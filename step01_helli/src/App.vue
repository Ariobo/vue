<template>
  <div id="app">
    <h1>Vue js 사작합니다</h1>
    <button v-on:click="clicked">눌러보셈</button>
    <!--@event명="콜백함수명"-->
    <button @click="clicked">눌러보셈2</button>
    <!-- msg 라는 모델을 innerText 로 출력하는 두가지 방법 -->
    <p>{{msg}}</p>
    <p v-text="msg"></p>
    <input type="text" v-model="myName" placeholder="이름 임력">
    <p>당신의 이름은 <strong>{{myName}}</strong> 입니다</p>
    <p>당신의 이름은 <strong v-text="myName"></strong> 입니다</p>
    <MyComponent/>
    <!-- v-bind 생략이 가능 -->
    <FortuneComponent v-bind:fortune="fortuneToday"/>
    <FortuneComponent :fortune="fortuneToday"/>
  </div>
</template>

<script>
  //component 하위에 MyComponent.vue 파일을 import 해서 MyComponent로 사용하겠음
  import MyComponent from "./components/MyComponent.vue";
  import FortuneComponent from "./components/FortuneComponent.vue";

export default {
  name: 'App',
  components:{
    MyComponent,
    FortuneComponent
},
  data(){
    //data() 함수에서 리턴하는 object 가 model 목록이 된다
    return {
      msg:"안녕하세요",
      myName:"",
      fortuneToday:"동쪽으로가면 귀인을 만나요"
    };
  },
  methods:{
    clicked(){
      alert("버튼 눌러 버렸어")
    }
  }
}
</script>

<style>
@import url(https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css);
</style>

