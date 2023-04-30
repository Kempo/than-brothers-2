<template>
  <div style="display: block">
    <div class="container">
      <div class="banner">
        <p class="text">
          <span><b>TEMPORARY HOURS: </b> 8PM CLOSE EVERYDAY</span>
          <span class="separator">&nbsp;|&nbsp;</span>
          <span>DINE-IN & TAKEOUT</span>
        </p>
      </div>
      <img
        class="half-circle"
        src="../assets/half-circle.svg"
        alt="Red Half Circle"
      />
      <div class="layout">
        <div class="header">
          <h2 class="title">
            <a href="/">
              <span class="first">PHO</span>
              {{ "" }}
              <span class="second">THAN BROTHERS</span>
            </a>
          </h2>
          <h2 class="nav">
            <a class="link" href="#menu"> menu </a>
            <a class="link" href="#location"> locations </a>
            <a class="link" href="#contact"> contact </a>
          </h2>
          <span class="mobile-divider" />
        </div>
        <div class="content">
          <div class="description">
            <div class="statement">
              <h1>Delicious,<br />Authentic,<br />And Affordable.</h1>
            </div>
            <div class="about">
              <h2>Serving the Greater Seattle region since 1996.</h2>
              <p>
                <strong>Pho</strong> is a Vietnamese rice noodle soup that
                invigorates and warms the soul. <br />
                <br />
                Try our homemade broth along with our selection of delicious
                beef cuts or vegetarian combinations.
              </p>
              <a href="#menu"><button>See Menu</button></a>
            </div>
          </div>
          <div class="media">
            <p class="promotion">AS FEATURED IN</p>
            <img class="down-arrow" src="@/assets/arrow.svg" alt="Grey Arrow" />
            <div class="refs">
              <a
                target="_blank"
                rel="noopener noreferrer"
                href="https://www.seattletimes.com/life/travel/gloom-got-you-down-try-these-8-tropical-escapes-in-the-seattle-area/"
                ><img src="@/assets/news/seattletimes.svg" alt="Seattle Times"
              /></a>
              <a
                target="_blank"
                rel="noopener noreferrer"
                href="https://www.bonappetit.com/people/article/macklemore-loves-pho"
                ><img src="@/assets/news/bonappetit.svg" alt="Bon Appetit"
              /></a>
              <a
                target="_blank"
                rel="noopener noreferrer"
                href="https://www.thrillist.com/eat/nation/best-west-coast-chain-restaurants-fast-food"
                ><img
                  style="background-color: red"
                  src="@/assets/news/thrillist.svg"
                  alt="Thrillist Media"
              /></a>
              <a
                target="_blank"
                rel="noopener noreferrer"
                href="https://www.seattleweekly.com/food/the-9-best-soups-for-surviving-winter-in-seattle/"
                ><img
                  src="@/assets/news/seattleweekly.svg"
                  alt="Seattle Weekly"
              /></a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss">
.half-circle {
  z-index: -1;
  position: absolute;
  left: 0px;
}

@media screen and (max-width: 499px) {
  .half-circle {
    top: 75%;
    transform: scale(6, 5);
  }
}

// 24 x 20
// 12 x 10

@media screen and (min-width: 500px) {
  .half-circle {
    bottom: 25%;
    transform: scale(12, 10);
  }
}

// DEFAULT STYLES
.container {
  .banner {
    z-index: 1;
    background-color: $banner-color;
    box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.1);
    color: white;
    letter-spacing: 1px;
    padding: 5px 0px;

    top: 0px;
    position: fixed;
    width: 100%;
  }

  .layout {
    .header {
      .title {
        text-transform: uppercase;
        letter-spacing: 2px;

        .first {
          color: $blue;
        }
        .second {
          color: $red;
        }
      }

      .nav {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        width: 100%;
        max-width: 350px;
      }
    }

    .content {
      margin: 0px 20px;

      .description {
        text-align: left;
        margin: 75px 0px;

        .about {
          width: 400px;

          h2 {
            font-size: 1.5em;
            font-weight: 600;
          }

          button {
            display: inline-block;
            font-size: 0.75em;
            font-weight: 300;
            letter-spacing: 2px;
            text-transform: uppercase;
            border-style: solid;
            border-color: $red;
            background-color: white;
            border-width: 1px;
            border-radius: 50px;
            padding: 10px;
            color: $red;
            transition: color 100ms, background-color 200ms;

            &:hover {
              color: white;
              background-color: $red;
            }
          }

          p {
            color: #7c7c7c;
          }
        }
      }

      .media {
        margin: 35px 0px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;

        .promotion {
          letter-spacing: 4px;
          font-weight: 400;
          color: #ccc;
          text-transform: uppercase;
        }

        .down-arrow {
          margin: 25px 0px 45px 0px;
        }

        .refs {
          a:hover {
            color: black;
          }
          img {
            width: auto;
            height: 45px;
            margin: 15px 15px;
          }
        }
      }
    }
  }
}

@media screen and (min-width: 770px) {
  h1 {
    font-size: 3.75em;
    margin-top: 0px;
  }

  .container {
    display: flex;
    flex-direction: column;
    justify-content: center;

    .banner {
      display: flex;
      justify-content: center;
    }

    .layout {
      align-self: center;

      .header {
        margin: 75px 20px 0px 20px;

        display: flex;
        flex-direction: row;
        flex-grow: 1;
        justify-content: space-between;
        align-items: center;

        .title {
          font-size: 1.75em;
        }

        .nav {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          width: 100%;
          max-width: 350px;
        }

        .mobile-divider {
          display: none;
        }
      }

      .content {
        .description {
          display: flex;
          flex-direction: row;
          justify-content: space-between;
          align-items: center;
        }
      }
    }
  }
}

@media screen and (max-width: 769px) {
  h1 {
    font-size: 2.25em;
  }

  .container {
    .banner {
      .text {
        display: flex;
        flex-direction: column;
        justify-content: center;

        .separator {
          display: none;
        }
      }
    }

    .layout {
      margin: 0px;

      .header {
        margin: 125px 20px 0px 20px;

        display: flex;
        flex-direction: column;
        align-items: center;

        .nav {
          display: flex;
          flex-direction: column;
          width: 100%;
          max-width: 350px;
          margin: 0px 0px 50px 0px;
        }

        .mobile-divider {
          display: block;
          height: 1px;
          width: 100px;
          background-color: #ccc;
        }
      }
    }
  }
}
@media screen and (max-width: 425px) {
  .container {
    .banner {
      .text {
        font-size: 0.85em;
      }
    }

    .layout {
      .content {
        .description {
          .about {
            width: auto;
          }
        }
      }
    }
  }
}

a:hover {
  color: $red;
}
</style>
