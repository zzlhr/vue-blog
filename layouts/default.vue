<template>
  <div>
    <div class="text-center blog-title">
      <b-img rounded="circle" src="https://avatars0.githubusercontent.com/u/25954503?s=460&v=4" width="75" height="75" alt="img" class="m-1" ></b-img>
      <h2>刘浩然的博客</h2>
      <div></div>
    </div>
    <div class="blog-nav">
      <b-container>
        <b-nav>
          <b-nav-item @click="jump('/')" active>首页</b-nav-item>
          <b-nav-item @click="jump('/articles')">文章</b-nav-item>
          <b-nav-item @click="jump('/about')">关于</b-nav-item>
        </b-nav>
      </b-container>
    </div>
    <nuxt/>
    <div class="blog-footer text-center">
      <p class="">© 2018 刘浩然的博客.</p>
    </div>
  </div>
</template>
<style>
  @import url('https://fonts.googleapis.com/css?family=Acme|Asap|Cabin+Sketch|Kalam|Poiret+One');
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif,
  'Cabin Sketch', cursive,'Kalam', cursive, 'Poiret One', cursive,'Acme', sans-serif,'Asap', sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
  color: #47494e;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}


.button--green {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #3b8070;
  color: #3b8070;
  text-decoration: none;
  padding: 10px 30px;
}

.button--green:hover {
  color: #fff;
  background-color: #3b8070;
}

.button--grey {
  display: inline-block;
  border-radius: 4px;
  border: 1px solid #35495e;
  color: #35495e;
  text-decoration: none;
  padding: 10px 30px;
  margin-left: 15px;
}

.nav-item>.active{
  background: rgba(0, 132, 255, 0.1);;
  color: #0084ff;;
}
.button--grey:hover {
  color: #fff;
  background-color: #35495e;
}
</style>
<script>
  export default {
    data(){
      return{

      }
    },
    methods:{
      jump(url){
        location.href=url;
      }
    }

  }
</script>
