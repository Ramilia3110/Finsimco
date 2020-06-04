<template>
  <div class="team">
    <div class="container">
      <h1>Meet the team</h1>
      <div class="card-container">
        <div class="card" v-for="card in cards" :key="card.staffId">
          <div class="card__upper">
            <div class="card__img">
              <img v-bind:src="card.staffImg" />
            </div>
          </div>
          <div class="card__lower">
            <div class="content">
              <h3>{{ card.name }}</h3>
              <h4>{{ card.position }}</h4>
              <p>{{ card.staffBG }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cards: [
        {
          staffId: 1,
          staffImg: require("@/assets/p1.png"),
          name: "Gerhard Wörtche",
          position: "Co-Founder",
          staffBG:
            "Gerhard has various front-office analytical experience including sell-side and buy-side roles at Morgan Stanley, Deutsche Bank, S&P and HPS Investment Partners. He holds a PhD in Quantitative Finance.  "
        },
        {
          staffId: 2,
          staffImg: require("@/assets/p2.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 3,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 4,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 5,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 6,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 7,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        },
        {
          staffId: 8,
          staffImg: require("@/assets/p3.png"),
          name: "Ruby Deet",
          position: "Co-Founder",
          staffBG:
            "Besides roles as senior strategy consultant and senior analyst at S&P, Sanjay has various entrepreneurial experience. He studied Mathematics at Cambridge and qualified as an actuary in four years."
        }
      ]
    };
  }
};
</script>

<style lang="scss" scoped>
.team {
  width: 100%;
  margin: 0;
  padding: 3rem 0 3rem 0;

  h1 {
    padding: 5rem 0 1rem 4.2rem;
    font-size: 8rem;
    font-weight: 400;
    text-align: left;
    margin-bottom: 7rem;
    color: #01c9dc;
  }
}
.container {
  width: 70%;
  margin: 0 auto;
}
.card-container {
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: center;
}
.card {
  width: 27rem;
  height: 32rem;
  background: #fbfcfc;
  box-shadow: 0 0 0.3rem #000000b3;
  margin: 2rem;
  border-radius: 1rem;

  transition: all 2s ease-in;

  &:hover .card__upper {
    background: rgb(14, 180, 192);
  }
  &:hover .card__img img {
    transform: scale(1.15);
  }
  &__upper {
    height: 8rem;
    padding: 0;
    background: #01c9dc;
    border-radius: 1rem 1rem 0 0;
  }
  &__lower {
    height: 24rem;
    text-align: center;
  }
}
.content {
  padding: 0 3rem 3rem 3rem;
}
h3 {
  margin-top: 3.9rem;
  font-size: 1.8rem;
  color: #01c9dc;
}
h4 {
  font-size: 1.5rem;
  font-weight: 200;

  color: #4c4d4d;
}
p {
  text-align: justify;
  font-size: 1.4rem;
  line-height: 1.8rem;
  margin-top: 1.5rem;
}

.card__img {
  background: #fff;
  width: 9rem;
  height: 10rem;
  border-radius: 50%;
  padding: 5px;
  transform: translate(9rem, 2rem);
  z-index: 2;
  img {
    width: 100%;
    height: 100%;
    border-radius: 50%;
  }
}
@media only screen and (max-width: 992px) {
}
@media only screen and (max-width: 768px) {
  #staff-cards {
    h1 {
      font-size: 3rem;
    }
  }
  card-container {
    flex-direction: column;
  }
}
</style>
