<template>
  <div class="hero">
    <div class="video-wrapper">
      <video autoplay muted loop id="bgVideo">
        <source src="@/assets/1.mp4" type="video/mp4" />
      </video>
      <div class="container">
        <div class="img-box">
          <img src="@/assets/hero1.svg" />
        </div>
        <div class="content">
          <h1>Join the top financial analysts.</h1>
          <p>
            Real-life investment banking simulations to forge tomorrow’s market leaders. We&#39;re working
            with the leading banks on their staff training and development.
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.video-wrapper {
  background: rgba($color: #000, $alpha: 0.5);
  position: relative;
  width: 100%;
  height: 100vh;
  overflow: hidden;
  video {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%) translateY(-50%);
    min-width: 100%;
    min-height: 100%;
    width: 100vw;
    height: auto;
    z-index: -1;
    overflow: hidden;
    object-fit: cover;
  }
}
.container {
  position: relative;
  width: 70%;
  margin: 9rem auto;
  padding: 5rem 0 3rem 0;
}
.img-box {
  position: relative;
  float: right;
  width: 40rem;
  height: 40rem;
  border-radius: 50%;
  margin: 3rem;
  shape-outside: circle();

  img {
    margin-top: 5rem;
    width: 100%;
    height: 100%;
  }
}
.content {
  color: #fff;
  text-align: left;
  padding-top: 10rem;
  h1 {
    padding: 0 7rem 2rem 1rem;

    font-size: 5rem;
    font-weight: 700;
    line-height: 5.2rem;
    letter-spacing: 0.5rem;
  }
  p {
    font-size: 3.5rem;
    font-weight: 400;
  }
}

@media only screen and (max-width: 910px) {
  .container {
    width: 95%;
  }
  .content {
    padding-left: 3rem;
    h1 {
      font-size: 3rem;
      line-height: 3rem;
    }
    p {
      font-size: 2rem;
    }
  }
  .img-box {
    width: 35rem;
    height: 35rem;
  }
}
@media only screen and (max-width: 468px) {
  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    .content {
      order: 1;
    }
    .img-box {
      order: 2;
    }
  }
}
</style>