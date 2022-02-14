<template>
  <header class="vh-100 w-100 py-5 px-3">
      <nav class="container d-flex justify-content-between justify-content-md-start align-items-center">
          <a href="#">
            <img src="/images/logo.svg" alt="logo">
          </a>

          <ul class="d-none d-md-block d-md-flex gap-4 ms-5">
              <li class="text-white" v-for="list in lists" :key="list.id">{{list.title}} <span>
                  <img :src="list.icon" :alt="list.title"></span>
              </li>
          </ul>

          <div class="d-none d-md-block buttons d-md-flex align-items-center ms-auto gap-3">
            <a href="#" class="login text-white">Login</a>
            <a href="#" class="btn fw-bold" style="background-color: #fff; color: var(--clr-light-red);">Sign Up</a>
          </div>

          <a class="d-block d-md-none" href="#" @click="toggle">
              <img v-if="!iconClose" src="/images/icon-hamburger.svg" alt="menu">

              <img v-else src="/images/icon-close.svg" alt="menu-close">
          </a>
      </nav>

      <div class="header-text">
          <h1 class="title fs-1">
              A modern publishing plataform
          </h1>

          <p class="sub m-3">
              Grow your audience and build your online brand
          </p>

          <div class="buttons d-flex justify-content-center gap-3">
              <a href="#" class="btn btn-start">
                Start for free
              </a>

              <a href="#" class="btn btn-learn">
                  Learn More
              </a>
          </div>
      </div>

      <div v-if="menuBtn" class="menu-mobile px-4 py-2">
          <ul class="p-0 text-center">
              <li v-for="list in lists" :key="list.id">{{list.title}} <span>
                  <img :src="list.icon" :alt="list.title"></span>
              </li>

              <ul class="p-0 menu-connect">
                  <li>Contact</li>
                  <li>Newsletter</li>
                  <li>Linkedin</li>
              </ul>
          </ul>

          <hr>

          <div class="buttons d-flex flex-column text-center gap-3">
              <a href="#" class="login">Login</a>
              <a href="#" class="btn btn-sign">Sign Up</a>
          </div>
      </div>
  </header>
</template>

<script>
export default {
    data() {
        return {
            iconClose: false,
            menuBtn: false,
            lists: [
                {title: "Product", icon: "/images/icon-arrow-light.svg"},
                {title: "Company", icon: "/images/icon-arrow-light.svg"},
                {title: "Connect", icon: "/images/icon-arrow-light.svg"},
            ]
        }
    },

    methods: {
        toggle() {
            this.menuBtn = !this.menuBtn;
            this.iconClose = !this.iconClose;
        }
    }
}
</script>

<style scoped>
header {
    background-image:url("/images/bg-pattern-intro-mobile.svg"), linear-gradient(to bottom, var(--clr-bg-light-red), var(--clr-bg-red));
    background-position-x: 34%;
    background-position-y: 40%;
    border-bottom-left-radius: 30%;
}

nav {
    position: relative;
}

.menu-mobile {
    background-color: var(--clr-white);
    width: 95%;
    margin: 0 auto;
    position: absolute;
    top: 6.9rem;
    left: 50%;
    transform: translate(-50%, 0%);
}

.menu-mobile ul > li {
    padding: 12px 0;
    cursor: pointer;
}

.menu-connect {
    background-color: var(--clr-grayish-blue);
    border-radius: 10px;
}

.login {
    color: var(--clr-very-dark-black-blue);
    font-size: 18px;
    font-weight: bold;
}

.btn-sign {
    background-image: linear-gradient(to bottom, var(--clr-bg-light-red), var(--clr-bg-red));
    color: var(--clr-white);
    font-weight: bold;
    width: max-content;
    margin: 0 auto;
    padding: 8px 12px;
    display: block;
}

.header-text {
    max-width: 100%;
    margin: 0 auto;
    text-align: center;
    margin-top: 6.9rem;
    color: var(--clr-white);
}

.title {
    font-size: 33px;
}

.btn {
    padding: 8px 24px;
    border-radius: 10px;
}

.btn-start {
    color: var(--clr-light-red);
    background: var(--clr-white);
}

.btn-learn {
    border: 1px solid var(--clr-white);
    color: var(--clr-white);
}
</style>