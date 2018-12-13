<template>
  <div id="app">
    <div id="nav" class="nav">
      <div class="navleftBox"><router-link to="/" class="logo">Logo</router-link></div>
      <div class="searchBox"><input type="text" placeholder="search..." class="searchText"></div><button type="button" class="searchButton">Search</button>
      <div class="navrightBox">
        <router-link to="/VUpload" class="uploadButton">영상 업로드</router-link> | 
        <router-link to="/login" class="loginButton">로그인</router-link>
      </div>
    </div>
    <div id="category">
      
    </div>
    <div id="section" class="section">
    </div>
    <router-view/>
  </div>
</template>

<style>
  * {
    padding: 0;
    margin: 0;
  }

  a {
    text-decoration: none;
  }

  .nav {
    padding : 15px 0;
    overflow: hidden;
    border-bottom: 2px solid black;
    border-width: 50%;
  }

  .navleftBox {
    float: left;
    margin-left: 50px;
  }

  .searchBox {
    float: left;
    margin-left: 27%;
    border : 1px solid black;
    width: 26%;
    border-radius: 10px 0 0 10px;
  }

  .searchText {
    border: none;
    height: 30px;
    width: 100%;
    padding-left: 10px;
    font-size: 20px; 
    vertical-align: middle;
    border-radius: 10px 0 0 10px;
  }

  .searchButton {
    height: 32px;
    width: 80px;
    border-radius: 0 10px 10px 0;
  }

  .navrightBox {
    float: right;
    margin-right: 50px;
  }

  #category {
    width : 100%;
    height : 90px;
    border-bottom : 1px solid black;
    margin : 0 auto;
  }

  .section {
    height: 100%;
    width: 100%;
    background-color: rgba(68, 68, 68, 0.342);
  }
</style>