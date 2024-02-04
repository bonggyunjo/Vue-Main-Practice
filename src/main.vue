
<template>
  <div id="app">
    <!-- 모달창-->

    <div class="menu">
    <h4 ><a v-for="(menu, index) in menus" :key="menu" :href="menuLinks[index]">{{ menu }}</a></h4>
    <img class="scrap-image" src="/image/스크랩.png">
    <img class="alarm-image" src="/image/알람.png">
    <img class="mypage-image" src="/image/마이페이지.png">
    </div> 

    <!-- 헤더 부분 글 작성 버튼-->
    <div id="header-board-write" class="btn-group">
  <button type="button" class="btn btn-secondary dropdown-toggle" data-bs-toggle="dropdown" aria-expanded="false">
    글쓰기
    <span class="visually-hidden">Toggle Dropdown</span>
  </button>
  <ul class="dropdown-menu">
    <li v-for="(item, index) in menuItems" :key="item.text">
    <a class="dropdown-item" id="menu-font" style="text-align: center;" href="#">
        <img :class="item.class" :src="item.imgSrc">{{ item.text }}
    </a>
    <hr class="dropdown-divider" v-if="index < menuItems.length - 1">
</li>
</ul>
   </div>
 <!-- 헤더와 바디 부분 사이 밑줄-->
   <div class="header-line"> 
    </div>

   <div id="carouselExampleDark" class="carousel slide" data-bs-ride="carousel">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active" data-bs-interval="4000">
      <img  src="/image/banner1.jpg" class="d-block w-100" style=" background-color: lightgray;  height:610px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <p style="position: relative; top:20px;">웹 사이트를 방문해주셔서 감사합니다.</p>
      </div>
    </div>
    <div class="carousel-item" data-bs-interval="4000">
      <img class="d-block w-100" style=" background-color: lightgray;  height:610px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5 style="position: relative; top: -200px;">공모전</h5>
        <p  style="position: relative; top:-200px;">content</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="/image/banner3.png" class="d-block w-100" style=" height:610px;" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <p  style="color:black; position: relative top:20px; font-weight:bolder;">웹 사이트를 방문해주셔서 감사합니다.</p>
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
        menus : ['.ZIP','스마트 인테리어','커뮤니티','가이드&팁스','.zip'],
        cards: [
        { title: 'Card title 1', text: 'content 1' },
        { title: 'Card title 2', text: 'content 2' },
        { title: 'Card title 3', text: 'content 3' },
        { title: 'Card title 4', text: 'content 4' },       
      ],
      menuItems: [
        { text: '일반 게시판', imgSrc: '/image/일반 게시판.png', class: 'board-image' },
        { text: '중고 게시판', imgSrc: '/image/중고 게시판.png', class: 'board-image' },
        { text: '일반 게시판 글쓰기', imgSrc: '/image/일반 글쓰기.png', class: 'write-image' },
        { text: '중고 게시판 글쓰기', imgSrc: '/image/중고 글쓰기.png', class: 'write-image' },
    ],
    menuLinks: ['#', '#', '#','#','#']
    };
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


