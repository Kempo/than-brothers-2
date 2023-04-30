<template>
  <div class="footer">
    <div class="top">
      <h2 class="title">
        <span class="first">PHO</span> <span class="second">THAN BROTHERS</span>
      </h2>
      <div class="nav">
        <ul>
          <li><a href="#menu">Menu</a></li>
          <li><a href="#location">Locations</a></li>
          <li><a href="#contact">Contact</a></li>
        </ul>
      </div>
    </div>
    <div class="copyright">
      <p>© 2020 Pho Than Brothers</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@media screen and (max-width: 500px) {
  .top {
    margin: 0px 20px;
  }

  .copyright {
    p {
      margin: 0px 20px;
    }
  }
}

@media screen and (min-width: 501px) {
  .top {
    margin: 0px 60px;
  }

  .copyright {
    p {
      margin: 0px 60px;
    }
  }
}

.footer {
  padding-top: 10px;
  border-top-style: solid;
  border-width: 3px;
  border-color: rgba(109, 158, 235, 0.08);
  text-align: left;

  .top {
    padding: 20px 0px;
    .title {
      font-size: 1em;
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
      ul {
        padding: 0px;
      }
      a:hover {
        color: $red;
      }
    }
  }

  .copyright {
    padding: 15px 0px;
    color: white;
    background-color: $banner-color;
  }
}
</style>
