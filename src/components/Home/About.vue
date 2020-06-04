<template>
  <div class="about">
    <div class="container">
      <h1>About Us</h1>
      <div class="about-us__container">
        <p>
          Finsimco is pioneering in investment banking simulations. Our
          simulations are the most challenging and realistic available for
          training corporate finance professionals.We provide experiential
          learning in an exciting, virtual business environment. The combination
          of immediate feedback and the competitive group dynamics are
          unbeatable for consolidating learning and acquiring skills. Our
          modular-based investment banking simulations are:
        </p>
        <ol class="list">
          <li>
            tailored to the target audience - intern, analyst and associate
            levels,
          </li>
          <li>available as a 1/2-day to 10-day product,</li>
          <li>
            flexible to allow the inclusion of further corporate finance fields
            besides the core M&A and Capital Markets modules.
          </li>
        </ol>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about {
  transition: all 500ms ease-in;
}
.container {
  width: 70%;
  margin: 0 auto;
  color: #01c9dc;
}
h1 {
  padding: 15rem 0 7rem 1rem;
  font-size: 8rem;
  font-weight: 400;
  text-align: left;
  width: 50%;
}
.about-us__container {
  margin: 0 0 5rem 0;
  padding: 0 2rem;
  -webkit-columns: 20rem 3;
  -webkit-column-gap: 5rem;
  -webkit-column-rule: 2px solid #01c9dc;
  p,
  li {
    font-size: 2rem;
    text-align: left;
  }
}

.list {
  margin-left: 2.3rem;
  // list-style: none;
}

@media only screen and (max-width: 768px) {
  .about-us__container {
    margin: 3rem 1.5rem 0 1.5rem;
  }
  .list {
    margin-left: 5rem;
  }
  h1 {
    padding: 7rem 0 0.5rem 3rem;
    font-size: 5rem;
    width: 100%;
  }
}
</style>
