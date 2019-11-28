<template>
  <div id="app">
    <nav id="site-navigation">
      <div id="topbar">
        <div class="inner nav-in">
          <div class="topbar-left block-alignment">
            <span>
              <i class="fa fa-envelope indent-sm"></i> coloponik@gmail.com
              <i class="fa fa-mobile-alt indent-sm" style="padding-left: 12px;"></i> +7 917 360 79 28
            </span>
          </div>
          <div class="topbar-right block-alignment">
            <span class="icons-topbar-style">
              <a href="#"><i class="fab fa-telegram-plane"></i></a>
              <a href="#"><i class="fab fa-facebook-f"></i></a>
              <a href="https://www.instagram.com/lissy___p/"><i class="fab fa-instagram"></i></a>
              <a href="https://m.vk.com/lissy_p"><i class="fab fa-vk"></i></a>
            </span>
          </div>
        </div>
      </div>

      <div class="block-alignment">
        <div id="main-bar" class="inner nav-in">
          <div class="logo block-alignment">
            <router-link to="/">Alpo</router-link>
          </div>
          <!-- <ul class="nav-menu nav justify-content-end block-alignment">
            <li class="nav-item indent-xl">
              <router-link class="nav-link active" to="/">Home</router-link>
            </li>
            <li class="nav-item indent-xl nav-link active">
              <router-link class="nav-link active" to="/account:id">Menu</router-link>
            </li>
            <li class="nav-item">
              <router-link class="nav-link active" to="/login"><i class="fas fa-user-alt"></i>
              </router-link>
            </li>
          </ul> -->

          <ul class="nav-menu nav justify-content-end block-alignment">
            <li class="nav-item" v-for="link in links" :key="link.title">
              <router-link class="nav-link active" :to="`${link.url}`">
                <i v-if="link.url == '/account/:id'" class="fas fa-user-alt"></i>{{link.title}}
              </router-link>
            </li>
          </ul>

        </div>
      </div>
    </nav>

    <router-view />
  </div>
</template>

<script>
  export default {
    data() {
      return {
        links: [
          { title: 'Home', url: '/' },
          { title: 'Menu', url: '/menu' },
          { url: '/account/:id' }
        ],
      }
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    font-family: 'Raleway', sans-serif;
  }

  *,
  *:before,
  *:after {
    box-sizing: border-box;
  }

  :any-link {
    color: #0ac5d6;
  }

  :any-link:hover {
    /* color: rgba(212, 194, 154, 0.959); */
    color: #c7b299;
    /* color: rgb(226, 180, 30); */
  }

  #site-navigation {
    position: fixed;
    width: 100%;
    color: #0ac5d6;
    z-index: 1;
  }

  #topbar {
    height: 30px;
    font-size: 12px;
    border-bottom: 0.3px solid #0ac5d6;
    /* border-bottom: 0.3px solid rgba(57, 212, 233, 0.959); */
  }

  #main-bar {
    height: 60px;
  }

  .inner {
    width: 100%;
    height: 100%;
    margin: 0 auto;
    padding: 0 20px;
    position: relative;
  }

  .nav-in {
    max-width: 1240px;
  }

  .navbar-inner {
    background: transparent;
  }

  .topbar-left {
    height: inherit;
    float: left;
  }

  .topbar-right {
    height: inherit;
    float: right;
  }

  .block-alignment {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .indent-sm {
    padding-right: 4px;
  }

  .indent-xl {
    padding-right: 40px;
  }

  .icons-topbar-style i {
    font-size: 15px;
    margin-left: 6px;
  }

  .logo {
    height: inherit;
    float: left;
    font-size: 20px;
  }

  .nav-menu {
    float: right;
    height: inherit;
    font-size: 14.5px;
  }

  .block-format {
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;
    width: 100%;
  }
</style>