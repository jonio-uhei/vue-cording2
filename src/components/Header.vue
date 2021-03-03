<template>
<div class="header-wrap">
  <header class="header">
    <div class="header__menu">
      <h1><a href="#"><img class="header-logo" src="@/assets/images/logo.png" alt=""></a></h1>
      <div class="line"
        @click="naviOpen"
        :class="{'is-active':active}"
      ><!--/.header__menu-->
        <span></span>
        <span></span>
        <span></span>
      </div>
      <nav class="navi-pc">
        <ul class="navi__flexbox">
          <li><a href="#">企業理念</a></li>
          <li><a href="#">施工事項</a></li>
          <li><a href="#">採用情報</a></li>
          <li><a href="#">お問い合わせ</a></li>
        </ul><!--/.navi__flexbox-->
      </nav><!--/.navi-pc-->
    </div><!--/.header__menu-->
    <transition name="navi">
      <nav class="navi" v-show="navi">
        <ul class="navi_wrap">
          <li><a href="#">企業理念</a></li>
          <li><a href="#">施工事項</a></li>
          <li><a href="#">採用情報</a></li>
          <li><a href="#">お問い合わせ</a></li>
        </ul><!--/.navi_wrap-->
      </nav><!--/.navi-->
    </transition>
    
  </header><!--/.header-->
  <p class="firstview-title">街を作る。未来を作る。</p>
</div><!--/.header-wrap-->
</template>

<script>
  export default{
    data:function(){
      return{
        active:false,
        navi:false
      }
    },
    methods:{
      naviOpen(){
        this.active = !this.active;
        this.navi = !this.navi;
      }
    }
  }
</script>

