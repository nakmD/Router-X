<template>
  <div class="home">
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <header>
      <div class="header-wrap d-flex align-items-center">
        <h1 class="logo">
          <a href="#" style="font-size: 1.4rem;">FanMusic</a>
        </h1>
        <div class="header-humberger">
          <span></span>
        </div>
        <nav>
          <ul class="header-menu list-unstyled">
            <li>
              <a href="#">米津玄師</a>
            </li>
            <li>
              <a href="#">ONE OK ROCK</a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
    <div id="demo">
      <hooper :progress="true" :autoPlay="true" :playSpeed="2000">
        <slide>
          好きなアーティストの情報を知ろう！
        </slide>
        <slide>
          好きなアーティストの同じファンの人と話そう！
        </slide>
        <slide>
          新しく好きなアーティストを見つけよう
        </slide>
      </hooper>
      <!-- <p class="animate__animated animate__fadeInTopLeft">好きなアーティストの情報を知ろう！</p>
      <p class="animate__animated animate__fadeInTopLeft">好きなアーティストの同じファンの人と話そう！</p>
      <p class="animate__animated animate__fadeInTopLeft">新しく好きなアーティストを見つけよう</p> -->
    </div>

  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  // components: {
  //   HelloWorld
  // }
}
</script>

<style scoped>
@media (min-width: 940px) {
  header {
    box-sizing: content-box;
    height: 94px;
    border-bottom: 1px solid #ccc;
    font-family: "ヒラギノ角ゴ Pro W3","Hiragino Kaku Gothic Pro","Meiryo UI","メイリオ",Meiryo,"游ゴシック","Yu Gothic","游ゴシック体",YuGothic,"ＭＳ Ｐゴシック","MS PGothic",HelveticaNeue-Regular,sans-serif;
  }

  header .header-wrap {
    position: relative;
    padding: 0;
    height: 10vh;
  }

  header .logo {
    flex-grow: 1;
    margin-left: 30px;
  }

  header .header-humberger {
    display: none;
  }

  header nav {
    /* display: -webkit-box; */
    display: -ms-flexbox;
    display: flex;
    margin-right: 233px;
    height: 100%;
  }

  header nav .header-menu {
    /* display: -webkit-box; */
    display: -ms-flexbox;
    display: flex;
    height: 100%;
    margin: auto;
  }

  .list-unstyled {
    padding-left: 0;
    list-style: none;
  }

  .header-menu li {
    height: 100%;
  }

  header nav .header-menu>li>a {
    font-size: .875rem;
    position: relative;
    display: inline-block;
    padding-right: 10px;
    padding-left: 10px;
    height: 100%;
    color: rgb(0, 0, 0);
    line-height: 10vh;
  }

  header nav .header-menu>li>a::after {
    position: absolute;
    bottom: 0;
    left: 0;
    display: inline-block;
    width: 0;
    height: 4px;
    background: linear-gradient(to bottom right,#004386,#008eee);
    content: "";
    opacity: 1;
    transition: all .3s;
  }
}

.hello {
  height: 100vh;
}

header {
  height: 10vh;
  background-color: rgb(250, 250, 250);
}

header .header-humberger {
  position: absolute;
  top: 50%;
  right: 18px;
  z-index: 100;
  display: block;
  /* -webkit-box-sizing: content-box; */
  box-sizing: content-box;
  margin-top: -11px;
  width: 30px;
  height: 22px;
  cursor: pointer;
}


.align-items-center {
  -webkit-box-align: center!important;
  -ms-flex-align: center!important;
  align-items: center!important;
}

.d-flex {
  display: -webkit-box!important;
  display: -ms-flexbox!important;
  display: flex!important;
}

header .logo a {
  display: block;
  width: 130px;
  height: 40px;
  background-size: contain;
  line-height: 42px;
  text-decoration: none;
}

header a:hover {
  color: inherit;
  text-decoration: none;
}

.list-unstyled {
  list-style: none;
}

a {
  color: inherit;
  word-break: break-word;
  -webkit-transition: all .3s;
  transition: all .3s;
  text-decoration: none;
}

a:hover {
  text-decoration: none;
  opacity: .5;
}

main {
  height: 90vh;
}

main > h1 {
  text-align: center;
}

/* @media (min-width: 768px) {

} */
@media (min-width: 768px) {
  #nav {
    padding: 3px;
  }

  #nav a {
    font-weight: bold;
    color: #2c3e50;
  }

  #nav a.router-link-exact-active {
    color: #42b983;
  }
}
</style>