<script>
  export let store;
  export let image;
  export let url;
  export let fblink;
  export let iglink;
  export let walink;
  export let linkwebsite;
  export let linkcatalogo;
  export let zonamall;
</script>

<style>
  .aligncenter {
    text-align: center;
  }

  .storeBox {
    background: #fff;
    padding: 10px;
    width: 30%;
    display: inline-grid;
    text-align: center;
    margin-left: 10px;
    margin-right: 10px;
    height: auto;
    vertical-align: top;
    border: 1px dotted #123352;
    margin-bottom: 30px;
    border-radius: 4px;
    box-shadow: 0px 3px 10px 0px #8d8d8d;
  }

  .storelogo {
    height: 150px;
    padding: 15px;
    overflow: hidden;
    text-align: center;
    margin-bottom: 0px;
  }

  .storelogo img {
    width: 90% !important;
  }

  .gridBtn {
    width: 180px;
    height: 40px;
    border-radius: 50px;
    margin: 0 auto;
    padding: 8px;
    text-align: center;
    background-color: #123352;
    color: white;
  }
  .socialMedia {
    margin-top: -10px;
    margin-bottom: 10px;
  }
  .socialMedia a {
    color: #989898;
    font-family: "Roboto" sans-serif;
    font-size: 19px;
  }

  .websitelink {
    font-weight: 600;
    color: #133352;
    font-family: Roboto;
  }

  .linkweb {
    font-weight: 500;
    color: #1f1752 !important;
    text-decoration: none;
  }
  .storeBox h2 {
    font-weight: 600;
    font-size: 34px;
    font-family: "Open Sans" sans-serif;
    color: #f9b217;
    text-transform: uppercase;
    margin-bottom: 25px;
  }

  @media only screen and (max-width: 950px) {
    .storeBox {
      width: 95%;
      display: inline-grid;
      text-align: center;
      margin-left: 10px;
      margin-right: 10px;
    }
    .storelogo {
      margin-bottom: 25px;
    }
  }

  .zonalink {
    margin-top: -10px;
  }
  .storeBox span {
    color: #032e58;
    font-size: 13cpx;
    font-weight: 600;
    margin-top: -10px;
  }
</style>

<div class="storeBox">
  <div class="storelogo">
    <img src={image} alt={store} width="100%" />
  </div>
  <a href="/#ubicaciones" class="zonalink">
    <span>"{zonamall}"</span>
  </a>
  <br />

  <div class="socialMedia">
    <img src="./img/wastore.png" alt="walink" />
    <a href="https://wa.me/504{walink}" target="_blank">{walink}</a>

    <br />
    <br />

    <a href={fblink} target="_blank">
      <img src="./img/fbstore.png" alt="fblink" />
    </a>
    <a href={iglink} target="_blank">
      <img src="./img/igstore.png" alt="instalink" />
    </a>
    <a href={linkwebsite} target="_blank">
      <img src="./img/website.png" alt="website" />
    </a>
    <hr />

    <a class="linkweb" href={url}>Más Información</a>
    <br />

  </div>
  <a class="gridBtn" href={linkcatalogo} target="_blank">Catálogo</a>
</div>
