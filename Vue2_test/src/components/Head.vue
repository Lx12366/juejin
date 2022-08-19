<template>
<div id="box">
  <div class="mask"></div>
  <form class="load">
    <div class="panfish">
      <img src="../assets/img/005.png">
      </div>  
      <div class="panel" style="  position: relative;">
        <span @click="back" class="back">X</span>
        <h1 class="title">手机登录</h1>
        <div class="input-group">
          <table class="loadTable">
            <tr>  
              <span>账号：<input type="text" placeholder="请输入手机号码" ></span>
            </tr>
            <tr>  
              <span>密码：<input type="password" placeholder="密码" ></span>
            </tr>
            <tr>
              <button @click="commit" class="loadCommit">登录</button>
            </tr>
          </table>
        
        </div>
      </div>
  </form>
  <div id="header">
    <div class="container">
      <div class="logo">
        <img src="../assets/img/002.png" alt="稀土掘金">
      </div>
      <div class="nav">
        <ul class="nav-list">
          <li class="main-nav-list">
            <ul class="nav-list-ul">
              <li class="nav-list-ul-li">首页</li>
              <li class="nav-list-ul-li">沸点</li>
              <li class="nav-list-ul-li">课程</li>
              <li class="nav-list-ul-li">直播</li>
              <li class="nav-list-ul-li">活动</li>
              <li class="nav-list-ul-li">商城</li>
              <li class="nav-list-ul-li">APP</li>
              <li class="nav-list-ul-li">插件</li>
              <li class="nav-img"><img height="40" width="115" src="../assets/img/001.png"></li>
            </ul>
          </li>
          <ul class="right-nav">
            <li class="searh-add">
              <ul class="right-nav-ul">
                <li class="nav-item">
                  <form class="search-form isResourceVisible">
                    <input type="search" maxlength="32" placeholder="探索稀土掘金" value class="search-input isResourceVisible">
                    <div class="seach-icon-centainer">
                      <img src="../assets/img/003.png" alt="探索" class="search-icon">
                    </div>
                    <div class="typehead" style="display:none">
                      <div class="title">
                        <span>搜索历史</span>
                        <span class="clear">清空</span>
                      </div>
                      <div class="list">
                        <div>字节跳动</div>
                      </div>
                    </div>
                  </form>
                </li>
                  <li class="nav-item add creator-item">
                  <div class="add-group">
                    <button class="add-btn">创造者中心</button>
                    <div class="more"></div>
                  </div>
            </li>
              </ul>
            </li>
          
            <li class="nav-item vip-entry">
              <div class="vip-title">
                <img src="../assets/img/004.png" class="vip-img">
                <div class="vip-words">会员</div>
              </div>
            </li>
            <li class="nav-item auth">
              <button @click="load" class="login-btn">登录</button>
            </li>
          </ul>
        </ul>
      </div>
    </div>
  </div>
  <div class="header-bottom">
    <ul class="h-b-ul">
      <li  class="h-b-ul-li"> 综合</li>
      <li  class="h-b-ul-li"> 后端</li>
      <li  class="h-b-ul-li"> 前端</li>
      <li  class="h-b-ul-li"> Androi</li>
      <li  class="h-b-ul-li"> IOS</li>
      <li  class="h-b-ul-li"> 人工智能</li>
      <li  class="h-b-ul-li"> 开发工具</li>
      <li  class="h-b-ul-li"> 代码人生</li>
      <li  class="h-b-ul-li">阅读</li>
    </ul>
  </div>
</div>
</template>

<script>
export default {
  name:'Head',
  methods:{
    load(){
      document.querySelector('.load').style.display = "block"
      let s = document.querySelector('.mask').style
      s.opacity=1
      s.zIndex =999
    },
    back(){
      document.querySelector('.load').style.display = "none"
      let s = document.querySelector('.mask').style
      s.opacity=0
      s.zIndex =-1
    },
    commit(){

    }
  }
} 
</script>

<style>
.loadTable>span>input{
   width: 100%;
}
.loadTable{
  width: 260px;
  height: 260px;
}
.panfish img{
  position: absolute;
   transform: translateX(-50%);
  top: -85px;
  left: 50%;
}
.back{
  position: absolute;
  right: 9rem;
  top: 1rem;
  font-size: 2rem;
  cursor: pointer;
}
.back:hover{
  color: blue;
}
.loadCommit{
  width: 100%;
  background: blue;
  color: white;
  border: none;
}
.load{
  position:fixed;
  top: 30%;
  left: 50%;
  transform: translateX(-50%);
  width: 320px;
  height: 300px;
  background: white;
  display: none;
  z-index: 999;
}
  .box.mask{
    width: 100%;
    height: 100%;
  }
  .mask{
        opacity: 0;
            width: 100%;
            height: 100%;
            position: fixed;
            left: 0;
            top: 0;
            transition: all 2s;
            /* background-image: linear-gradient(
                transparent,
                rgba(0,0,0,.5)
            ); */
            background-color: rgba(0, 0, 0, .6);
            z-index: -1;
  }
  #header{
    color: #909090;
    border-bottom: 1px solid #f1f1f1;
    height: 5rem;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    transition: all .2s;
    transform: translateZ(0);
  }
  .header-bottom{
     color: #909090;
    border-bottom: 1px solid #f1f1f1;
    height: 4rem;
    position: fixed;
    top:5rem;
    left: 0;
    right: 0;
  }
  .h-b-ul{
    display: flex;
        max-width: 960px;
    align-items: center;
    margin-left: 400px;
    height: 100%;
  }
  .h-b-ul-li{
    height: 100%;
    cursor: pointer;
    line-height: 4rem;
    font-size: 1.3rem;
    width: 7rem;
    text-align: center;
  }
   .h-b-ul-li:nth-child(1){
     color:blue
   }
   .h-b-ul-li:hover{
     color: blue;
   }
  .logo{
    margin-right: 1rem;
    display: flex;
    justify-content: center;
    height: 5rem;
    width: auto;
    align-items: center;
  }

   .container{
    position: relative;
    width:100%;
    display: flex;
    margin-left: 250px;
  }
  .nav-list{
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: relative;
    flex-direction: row-reverse;
    height: 100%;
    margin: 0;
  }
  .main-nav-list{
    display: flex;
    order: 99;
  }
  .nav-list-ul{
    display: flex;
  }
  .nav-list-ul-li{
    padding: 0;
    width:4rem;
    height: 5rem;
    color: black;
    font-size: 1.2rem;
    display: flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    position: relative;
  }
  .nav-list-ul-li:nth-child(1){
    color: blue;
  }
  .nav-list-ul-li::after{
    content: " ";
    position: absolute;
    bottom: 0;
    left: 50%;
    transform: translateX(-50%);
    background: blue;
    width: 2rem;
    height: 0.2rem;
    display: none;
  }
  .nav-list-ul-li:hover::after{
    display: block;
  }
  .nav-list-ul-li:hover{
    color:black
  }
  .nav-img{
    display: flex;
    width: 140px;
    height: 5rem;
    align-items: center;
    justify-content: center;
  }

.right-nav{
  display: flex;
    align-items: center;
    justify-content: flex-end;
    position: relative;
    height: 100%;
    margin: 0;
    order: 0;
}

  .searh-add{
    flex: 1 1 auto;
    height: 5rem;
    display: flex;
    justify-content: flex-end;
  }
  .right-nav-ul{
        display: flex;
    justify-content: flex-start;
  }
  .nav-item{
    color: #86909c;
    padding: 0 1rem;
    font-size: 1.167rem;
    margin: 0;
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .nav-item .search{
    cursor: auto;
    padding-left: 0;
  }
.typehead{
    width: 100%;
    position: absolute;
    top: 105%;
    line-height: 2rem;
    left: 0;
    z-index: 1000;
    min-width: 6rem;
    font-size: 1rem;
    color: #869aab;
    list-style: none;
    text-align: left;
    border-radius: 0.17rem;
    box-shadow: 0 1px 2px 0 rgb(0 0 0 / 5%);
    border: 1px solid #ebebeb;
    background-color: #fff;
}

.typehead .title{
  border-bottom: 1px solid #ebebeb;
  padding: 0.5rem 1rem;
  display: flex;
  justify-content: space-between;
}

.typehead .title .clear{
  cursor: pointer;
  color :blue;
}
  .typehead .list{
    cursor: pointer;
    color:gray
  }
  .search-form{
    background-color: #fff;
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-radius: 4px;
    position: relative;
    height: 2.834rem;
    border: 1px solid #c2c8d1;
    transition: width .2s;
  }
  .isResourceVisible{
    width: 260px;
}
  .search-input{
        border: none;
    width: calc(100% - 44px);
    padding: 0.6rem 0 0.6rem 1rem;
    box-shadow: none;
    outline: none;
    font-size: 1.1rem;
    color: #8a919f;
    background-color: transparent;
    transition: width .3s;
  }
  .seach-icon-centainer{
    position: relative;
    left: -2px;
    width: 44px;
    height: 30px;
    background: var(--juejin-background);
    border-radius: 2px;
  }
  .search-icon{
        display: inline-block;
    width: 1.33rem;
    padding: 0 0.8333rem 0 0;
    cursor: pointer;
    margin: 7px 15px;
  }
  .add{
    cursor: default;
    width: 25rem;
    transition: width .3s;
    overflow: hidden;
    padding-left: 0;
  }
  .add-group {
    display: flex;
    align-items: center;
    position: relative;
    cursor: pointer;
    width: 115px;
    height: 3rem;
}
.add-group .add-btn {
    padding: 0 1rem;
    font-size: 1.167rem;
    border-top-right-radius: 0;
    border-bottom-right-radius: 0;
    white-space: nowrap;
}
.nav-item.add.creator-item {
    overflow: visible;
    width: 11rem;
    padding-left: 5px;
}
.add-group .add-btn, .add-group .more {
    height: 100%;
    color: white;
    background-color:blue;
    border-radius: 3px;
    transition: background-color .1s linear .05s;
}
.vip-entry .vip-title{
    display: flex;
    align-items: center;
}
.vip-entry .vip-img {
    width: 24px;
    height: 24px;
}
.vip-entry .vip-title .vip-words {
    color: #86909c;
    font-weight: 400;
    font-size: 14px;
    line-height: 22px;
    margin-left: 4px;
}
.auth{
  color: blue;
  padding: 0 0 0 .833rem;
}
.nav-item .login-btn{
    background: rgba(30,128,255,.05);
    border: 1px solid rgba(30,128,255,.3);
    border-radius: 4px;
    padding: .3rem 1.5rem;
    color: #007fff;
    line-height: 1.9rem;
    cursor: pointer;
    font-size: 14px;
    font-weight: 400;
    margin-right: 2rem;
    height: 3rem;
    cursor: pointer;
}
</style>