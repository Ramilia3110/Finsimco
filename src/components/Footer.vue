<template>
  <div class="footer">
    <div class="blog1">
      <div class="container">
        <div class="menu">
          <div class="box box1">
            <p>Finsimco</p>
            <div class="social-media">
              <a href class="facebook">
                <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'facebook-f' }" />
              </a>
              <a href="https://www.linkedin.com/company/28894396/admin/" id="linkedin">
                <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'linkedin-in' }" />
              </a>
              <a href="https://twitter.com/finsimco" id="twitter">
                <font-awesome-icon :icon="{ prefix: 'fab', iconName: 'twitter' }" />
              </a>
            </div>
          </div>
          <div class="box box2">
            <h4>Links</h4>
            <router-link to="/">Home</router-link>
            <router-link to="/careers">Careers</router-link>
            <router-link to="/privacy">Privacy</router-link>
            <router-link to="/privacy">Testimonials</router-link>
          </div>
          <div class="box box3">
            <h4>address</h4>
            <p>
              Finsimco
              <br />24 Frans Hals Court
              <br />87 Amsterdam Road
              <br />E14 3UX,
              London
              <br />UK
              <br />info@finsimco.com
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="blog2">
      <span>
        <font-awesome-icon :icon="{ prefix: 'far', iconName: 'copyright' }" />
      </span>
      <p>2020 by Finsimco</p>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
  components: {}
};
</script>

<style lang="scss" scoped>
.footer {
}
.blog1 {
  background: #01c9dc;
  color: #fff;
}
.container {
  width: 70%;
  margin: 0 auto;
  .menu {
    padding: 3rem 0;
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(22rem, 1fr));
    grid-gap: 3rem;
    align-items: start;
  }
}
.box {
  margin-right: 5rem;
  h4 {
    font-size: 1.8rem;
    text-transform: uppercase;
    font-weight: 400;
    margin: 2rem 0 3rem 0;
  }
}
.box1 {
  p {
    top: 0;
    font-size: 4.1rem;
    font-weight: 500;
    margin-bottom: 2rem;
  }
  .social-media {
    a {
      background: #fff;
      color: #01c9dc;
      border-radius: 50%;
      padding: 0.4rem 1rem;
      margin-right: 2rem;
      font-size: 1.5rem;
      text-align: center;
      &:hover {
        background: #01c9dc;
        color: #fff;
      }
    }
  }
}
#twitter {
  padding: 0.42rem 0.65rem;
}
#linkedin {
  padding: 0.42rem 0.8rem;
}

.box2 {
  display: flex;
  flex-direction: column;
  margin-top: 2rem;
  border-top: 3px solid #fff;
  a {
    text-decoration: none;
    color: #fff;
    margin-bottom: 0.7rem;
    font-size: 1.5rem;
    &.router-link-exact-active {
      color: #10eeee;
    }
  }
}
.box3 {
  margin-top: 2rem;
  border-top: 3px solid #fff;
  font-size: 1.5rem;
  line-height: 2rem;
}
.blog2 {
  text-align: center;
  font-size: 1.5rem;
  background: #fff;
  color: #202222;
  letter-spacing: 0.2rem;
  font-weight: 400;
  padding: 1.5rem;
  display: flex;
  justify-content: center;
  align-items: center;
  span {
    margin: 0.7rem 1rem 0 0;
  }
  p {
    margin-top: 0.5rem;
  }
}
</style>
