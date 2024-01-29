
<template>
  <div id="app">
    <!-- 모달창-->
    <div class="black-bg" v-if="modalframe==true">
      <div class= "white-bg">
        <h4>상세페이지임</h4>
        <p> 상세페이지 내용임</p>
        <button @click="modalframe=false">닫기</button>
      </div>
    </div>
    <div class="menu">
    <h4><a v-for ="menus in menus" :key="menus">{{  menus }}</a></h4>
    <img class="scrap-image" src="./image/스크랩.png">
    <img class="alarm-image" src="./image/알람.png">
    <img class="mypage-image" src="./image/마이페이지.png">
    </div>   

    <div class="banner">
    </div>

    <div class="card-view">
      <div class="card-list">
    <div class="card" v-for="(card, index) in cards" :key="index">
      <div class="card-body">
        <h5 class="card-title">{{ card.title }}</h5>
        <p class="card-text">{{ card.text }}</p>
        <a href="#" class="btn btn-primary" style="position: relative; top: 75px;">Go Anywhere</a>
      </div>
    </div>
      </div>     
    </div>

    <div class="main-banner">
    </div>

</div>
</template>

<script>

export default {  
  name: 'App',
  data() {
    return {
        // 여기에 데이터 보관하셈 
        modalframe : false,
        //  신고수 : 0,
        price : [60,70,80],
        menus : ['로고자리','스마트 인테리어','커뮤니티','가이드&팁스','.zip','게시글 작성'],
        cards: [
        { title: 'Card title 1', text: 'content 1' },
        { title: 'Card title 2', text: 'content 2' },
        { title: 'Card title 3', text: 'content 3' },
        { title: 'Card title 4', text: 'content 4' },
      ],
        // products : ['역삼동원룸','xxx원룸','aaa원룸'],  
    }
  },

  methods : {
   // increase(){
     // this.신고수 +=1;
      //console.log(this.신고수);
    //}  
  },

  components: {

  }
}

</script>
<style scoped>
@import './css/main.css';
</style>  


