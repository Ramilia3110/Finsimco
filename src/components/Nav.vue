<template>
  <div class="nav">
    <div class="menu" :class="{ change_color: scrollPosition > 50 }">
      <div class="container">
        <a class="logo" href="#">Finsimco</a>
        <input type="checkbox" id="chk" v-model="checkboxValue" />
        <label for="chk" class="show-menu-btn">
          <font-awesome-icon icon="ellipsis-v" />sss
        </label>
        <ul>
          <router-link :to="{ path: '/', hash: '#' }" @click.native="uncheck">Home</router-link>

          <router-link :to="{ path: '/', hash: '#about' }" @click.native="uncheck">About</router-link>
          <router-link :to="{ path: '/', hash: '#why-with-us' }" @click.native="uncheck">Why Us</router-link>

          <router-link
            :to="{ path: '/', hash: '#why-with-us' }"
            @click.native="uncheck"
          >How it works</router-link>

          <router-link :to="{ path: '/', hash: '#team' }" @click.native="uncheck">Team</router-link>

          <router-link :to="{ path: '/', hash: '#contact' }" @click.native="uncheck">Contact</router-link>

          <label for="chk" class="hide-menu-btn">
            <font-awesome-icon icon="times" />xxx
          </label>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      scrollPosition: null,
      checkboxValue: false
    };
  },
  methods: {
    updateScroll() {
      this.scrollPosition = window.scrollY;
    },
    uncheck() {
      this.checkboxValue = false;
    }
  },

  mounted() {
    window.addEventListener("scroll", this.updateScroll);
  }
};
</script>

<style lang="scss" scoped>
.isHidden {
  right: 0;
}
.nav {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 10;
}
.menu {
  width: 100%;
  margin-top: 5.5rem;
}
.container {
  width: 70%;
  margin: 0 auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 1.8rem;
}

.change_color {
  background-color: #01c9dc;
  margin-top: 0;
  transition: 0.5s ease-in;
}

.logo {
  color: #fff;
  text-decoration: none;
  font-size: 3.7rem;
  font-weight: 700;
}
ul {
  display: flex;
  justify-content: space-between;
  list-style: none;
  padding: 1.8rem 0;
  a {
    color: #fff;
    text-decoration: none;
    padding: 0 1rem;
    transition: 0.4s;
  }
}
.show-menu-btn {
  float: right;
  padding-right: 2rem;
}
.show-menu-btn,
.hide-menu-btn {
  transition: 0.4s;
  font-size: 1.8rem;
  cursor: pointer;
  display: none;
  color: #fff;
}

ul a:hover,
.show-menu-btn:hover,
.hide-menu-btn:hover {
  color: #3498db;
}

#chk {
  position: absolute;
  visibility: hidden;
  z-index: -1111;
}

@media only screen and (max-width: 910px) {
  .change_color {
    position: absolute;
    width: 100%;
    padding: 1.9rem;
    background: #01c9dc;
  }
  .container {
    width: 95%;
  }

  .show-menu-btn,
  .hide-menu-btn {
    display: block;
  }

  .logo {
    float: left;
    padding-left: 3rem;
    font-size: 3rem;
  }
  ul {
    width: 100%;
    height: 100vh;
    background: #01c9dc;
    position: fixed;
    top: 0;
    right: -100%;
    margin: 0;
    padding: 8rem 0;
    transition: 0.7s;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-around;
    .hide-menu-btn {
      position: absolute;
      top: 4rem;
      right: 4rem;
    }
  }

  #chk:checked ~ ul {
    right: 0;
  }
}

@media only screen and (max-width: 768px) {
  .container {
    display: initial;
  }
}
</style>