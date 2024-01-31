
<template>
  <div id="app">
    <!-- 모달창-->

    <div class="menu">
    <h4><a href="#" v-for ="menus in menus" :key="menus">{{  menus }}</a></h4>
    <img class="scrap-image" src="./image/스크랩.png">
    <img class="alarm-image" src="./image/알람.png">
    <img class="mypage-image" src="./image/마이페이지.png">
    </div> 
    <!-- 헤더 부분 글 작성 버튼-->
    <div id="header-board-write" class="btn-group">
  <button type="button" class="btn btn-secondary dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
    글 작성
    <span class="visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="dropdown-menu">
    <li><a class="dropdown-item" style="text-align: center;" href="#">일반 게시판</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" style="text-align: center;" href="#">중고 게시판</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">일반 게시판 글 작성</a></li>
    <li><hr class="dropdown-divider"></li>
    <li><a class="dropdown-item" href="#">중고 게시판 글 작성</a></li>
  </ul>
   </div>

   <div id="carouselExampleDark" class="carousel carousel-dark slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active" data-bs-interval="3000">
      <img  class="d-block w-100" style=" background-color: lightgray; width:300px; height:600px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5 style="position: relative; top: 50px;">First slide label</h5>
        <p style="position: relative top:20px;">content 1.</p>
      </div>
    </div>
    <div class="carousel-item" data-bs-interval="4000">
      <img class="d-block w-100" style=" background-color: lightgray; width:300px; height:600px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5 style="position: relative; top: 50px;">Second slide label</h5>
        <p  style="position: relative top:20px;">content 2.</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="./image/banner3.png" class="d-block w-100" style="width:300px; height:600px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5 style="position: relative; top: 50px;">Third slide label</h5>
        <p  style="position: relative top:20px;">content 3.</p>
      </div>
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
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
        menus : ['로고자리','스마트 인테리어','커뮤니티','가이드&팁스','.zip'],
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


