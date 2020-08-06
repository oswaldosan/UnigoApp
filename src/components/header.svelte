<script context="module">

</script>

<style>
  .headerMain {
    z-index: 99;
    position: relative;
    padding: 0px;
    height: 90px;
  }

  .logo {
    width: 115px;
    position: absolute;
    top: -10px;
    left: 4%;
    padding: 10px;
  }

  .logoimg {
    width: 100% !important;
  }

  .menuBox {
    font-family: "Roboto", sans-serif;
    text-transform: uppercase;
    position: absolute;
    width: 80%;
    background-color: #153252;
    color: aliceblue;
    top: 00px;
    right: 0px;
    height: 100%;
    padding-top: 35px;
    padding-left: 50px;
    border-bottom-left-radius: 50px;
    text-align: right;
  }

  .menuBox ul {
    display: flex;
  }

  .menuBox ul li {
    margin-left: 30px;
    margin-right: 30px;
    font-size: 16px;
    font-family: sans-serif;
    list-style: none;
    font-weight: 500;
  }
  .menuBox ul li a {
    color: #fff;
    transition: all 0.5s ease;
    text-decoration: none;
    font-family: "Roboto";
  }

  .menuBox ul li a:hover {
    color: #f9b218;
  }

  .navbar {
    display: none;
  }
  .normalLinks {
    display: block;
  }

  .navbar-light .navbar-toggler-icon {
    background-image: url(https://i.ya-webdesign.com/images/hamburger-menu-icon-png-white-12.png);
    background-size: 55px;
  }
  .bg-light {
    background-color: #153252 !important;
  }
  .nav-link {
    color: white !important;
  }
  .logomobile {
    display: none;
  }
  .socialiconsHeader {
    position: absolute;
    top: 25px;
    right: 25px;
  }

  @media only screen and (max-width: 950px) {
    .navbar {
      display: block;
    }
    .normalLinks {
      display: none !important;
    }

    .menuBox {
      font-family: "Roboto", sans-serif;
      text-transform: uppercase;
      position: absolute;
      width: 100%;
      background-color: #153252;
      color: aliceblue;
      top: 0px;
      right: 0px;
      height: 100%;
      padding-top: 15px;
      padding-left: 10px;
      border-bottom-left-radius: 10px;
      text-align: right;
    }
    .logoimg {
      display: none;
    }

    .logo {
      width: 115px;
      position: absolute;
      top: 7px;
      left: 2%;
      padding: 10px;
    }

    .logomobile {
      position: absolute;
      display: block;
      z-index: 999999;
      width: 60px;
      top: 1px;
    }
  }
</style>

<div class="headerMain">
  <div class="logo">
    <a href="/">
      <img alt="unigo logo " src="./img/logounigo.png" class="logoimg" />
      <img alt="unigo logo " src="./img/logomobile.png" class="logomobile" />
    </a>
  </div>

  <div class="menuBox">
    <div class="socialiconsHeader">
      <a href="https://www.facebook.com/uniplazahonduras/">
        <img src="./img/fbtop.png" alt="facebook" />
      </a>
      <a href="https://www.instagram.com/uniplazahn/">
        <img src="./img/twtop.png" alt="twitter" />
      </a>
      <a href="https://www.instagram.com/uniplazahn/">
        <img src="./img/igtop.png" alt="instagram" />
      </a>
    </div>
    <ul class="normalLinks">
      <li>
        <a href="/">Inicio</a>
      </li>

      <li>
        <a href="#about">¿Qué es?</a>
      </li>
      <li>
        <a href="#howto">¿Cómo funciona?</a>
      </li>
      <li>
        <a href="#ubicaciones">Ubicaciones</a>
      </li>
      <li>
        <a href="http://www.malluniplaza.com/contacto/">Contacto</a>
      </li>
    </ul>

    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation">
        <span class="navbar-toggler-icon" />
      </button>

      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mr-auto">
          <li class="nav-item active">
            <a class="nav-link" href="/">
              Inicio
              <span class="sr-only">(current)</span>
            </a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#about">¿Qué es?</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#howto">¿Cómo funciona?</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/#ubicaciones">Ubicaciones</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="http://www.malluniplaza.com/contacto/">
              Contacto
            </a>
          </li>
        </ul>

      </div>
    </nav>

  </div>

</div>
