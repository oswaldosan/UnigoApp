<script>
  import Header from "../components/header.svelte";
  import Footer from "../components/footer.svelte";
  import TopSlider from "../components/topSlider.svelte";
  import ZonaA from "../components/zonaUno.svelte";
  import ZonaUno from "../components/zonaUno.svelte";
  import ZonaDos from "../components/zonaDos.svelte";
  import ZonaTres from "../components/zonaTres.svelte";
  import { fade } from "svelte/transition";

  function myFunction() {
    var element = document.getElementById("pruebaj");
    element.classList.add("mystyle");
  }

  function scrollWin() {
    window.scrollTo(0, 0);
  }

  let selected;

  let hideA = false;
  let hideB = false;
  let hideC = false;

  let allZones = "verTodo";
  let zonaA = "ZonaA";
  let zonaB = "ZonaB";
  let zonaC = "ZonaC";

  function handleChange() {
    let selected = document.getElementById("selectoR").value;

    if (selected == "ZonaA") {
      hideA = false;
      hideB = true;
      hideC = true;
    } else if (selected == "ZonaB") {
      hideB = false;
      hideA = true;
      hideC = true;
    } else if (selected == "ZonaC") {
      hideC = false;
      hideA = true;
      hideB = true;
    } else if (selected == "verTodo") {
      hideA = false;
      hideB = false;
      hideC = false;
    }
  }
</script>

<style>
  .hide {
    display: none;
  }

  #myBtn {
    display: block;
    position: fixed;
    bottom: 20px;
    right: 30px;
    z-index: 99;
    font-size: 18px;
    border: none;
    outline: none;
    background-color: #003056;
    color: white;
    cursor: pointer;
    padding: 15px;
    border-radius: 4px;
  }

  #myBtn:hover {
    background-color: #ffb400;
  }

  h1 {
    text-align: center;
    font-family: Roboto;
    color: #153252;
    font-weight: 600;
    font-size: 30px;
  }

  .tiendas {
    background-image: url(/img/bodybgtiendas.png);
    background-size: contain;
    background-color: white;
    margin-top: 20px;
    border: 1px dotted #ccc;
    padding: 15px;
    font-family: Roboto;
    color: #153252;
  }
  .tiendas h1 {
    text-align: center;
    font-weight: 600;
    font-size: 30px;
  }
  .tiendas p {
    padding: 10px;
  }
  .preloader {
    width: 100%;
    margin: 0 auto;
    text-align: center;
  }

  .bodycontent {
    background-image: url("../img/bodybg.png");
    background-size: cover;
    background-repeat: no-repeat;
  }

  .textQue {
    display: inline-block;
    vertical-align: top;
    padding: 30px;
    width: 55%;
    margin: 10px;
  }
  .imageQue {
    display: inline-block;
    vertical-align: top;
    width: 40%;
    margin: 10px;
  }
  .icons {
    display: inline-block;
    vertical-align: top;
    width: 22%;
    margin: 15px;
    text-align: center;
  }
  .icons h2 {
    font-size: 23px;
    font-weight: 600;
  }
  .icons img {
    width: 110px;
  }
  .iconoSt {
    border: 2px solid #003056;
    padding: 25px;
    border-radius: 55px;
    margin-bottom: 25px;
  }

  @media only screen and (max-width: 950px) {
    .textQue {
      display: inline-block;
      vertical-align: top;
      padding: 10px;
      width: 100%;
      margin: 0 auto;
    }
    .imageQue {
      display: inline-block;
      vertical-align: top;
      width: 100%;
      margin: 0 auto;
    }
    .icons {
      display: inline-block;
      vertical-align: top;
      width: 40%;
      margin: 15px;
      text-align: center;
    }
    .icons h2 {
      font-size: 23px;
      font-weight: 600;
    }
    .icons img {
      width: 110px;
    }
    .iconoSt {
      border: 2px solid #003056;
      padding: 25px;
      border-radius: 55px;
      margin-bottom: 25px;
    }
  }

  .selectinput {
    position: relative;
    font-size: 24px;
    padding: 15px;
    border-radius: 4px;
    width: 300px;
    margin-top: 15px;
    margin-bottom: 55px;
    left: 50%;
    margin-left: -150px;
    text-align: center;
  }
</style>

<svelte:head>
  <title>UNIGO - Pide lo que quieras</title>
  <meta
    name="description"
    content="Portal digital en nuestra página Web, en donde todos los inquilinos
    y propietarios podrán promocionar sus tiendas y ventas en línea y formar
    parte de este modelo de negocio. " />
</svelte:head>

<main>
  <Header />
  <TopSlider />
  <br />
  <br />
  <button on:click={scrollWin} id="myBtn" title="Go to top">Top</button>

  <div class="container tiendas" id="about" transition:fade>

    <h1>¿QUÉ ES UNIGO?</h1>
    <hr />
    <div class="textQue">
      <p>
        Es un portal digital donde tu podrás visitarnos y realizar tus compras
        de una manera fácil y segura desde la comodidad de tú casa e ir a traer
        tus productos en las zonas UNIGO establecidas.
        <br />
        <br />
        Con nuestra iniciativa buscamos incrementar las ventas de nuestros
        socios comerciales e incrementar las visitas al mall en nuestras zonas
        de entrega.
      </p>
    </div>
    <div class="imageQue">
      <img src="/img/takeout.svg" alt="UNIGO" width="100%" />
    </div>
    <br />
    <br />

    <div id="howto" />
    <h1>¿Cómo funciona?</h1>
    <hr />

    <div class="icons">
      <img src="/img/icon1.png" alt="icon delivery" class="iconoSt" />
      <h2>Paso 1:</h2>
      Escoge tu tienda favorita, revisa los productos y contacta al número de la
      tienda para realizar tu pedido.
    </div>

    <div class="icons">
      <img src="/img/icon2.png" alt="icon delivery" class="iconoSt" />
      <h2>Paso 2:</h2>
      Visita Unimall y dirígete al área señalizada de UNIGO en cualquier de
      nuestras zonas establecidas en el estacionamiento.
    </div>

    <div class="icons">
      <img src="/img/icon3.png" alt="icon delivery" class="iconoSt" />
      <h2>Paso 3:</h2>
      Escribe a la tienda para que lleven tú compra y coordinar la entrega.
    </div>

    <div class="icons">
      <img src="/img/icon4.png" alt="icon delivery" class="iconoSt" />
      <h2>Paso No. 4:</h2>
      Llévate tú pedido
    </div>

  </div>

  <div class="container tiendas" id="ubicaciones" transition:fade>
    <h1>Ubicaciones</h1>
    <img src="/img/plano.jpg" alt="plano" width="100%" />

  </div>
  <br />
  <br />

  <div class="container aligncenter bodycontent">
    <h1>Selecciona la Zona</h1>
    <select
      on:change={handleChange}
      name="ZoneSelector"
      id="selectoR"
      class="selectinput">
      <option value={allZones}>Ver Todo</option>
      <option value={zonaA}>Zona A</option>
      <option value={zonaB}>Zona B</option>
      <option value={zonaC}>Zona C</option>
    </select>

    <div class:hide={hideA} transition:fade>
      <h1>Zona A</h1>
      <hr />
      <ZonaUno />
      <br />
    </div>

    <div class:hide={hideB} transition:fade>
      <h1>Zona B</h1>
      <hr />
      <ZonaDos />
      <br />
    </div>

    <div class:hide={hideC} transition:fade>
      <h1>Zona C</h1>
      <hr />
      <ZonaTres />
      <br />
    </div>

  </div>

</main>
<Footer />
