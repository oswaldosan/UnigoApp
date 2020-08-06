<script>
  import Header from "../components/header.svelte";
  import Tiendas from "../pages/tiendas.svelte";
  import Footer from "../components/footer.svelte";
  import TopSlider from "../components/topSlider.svelte";
  import GridStores from "../components/gridstores.svelte";
  import { onMount } from "svelte";

  const apiURL = "https://www.malluniplaza.com/wp-json/wp/v2/tiendasunigo";
  let data = [];

  onMount(async function () {
    const response = await fetch(apiURL);
    data = await response.json();
    console.log(data);
  });

  function myFunction() {
    var element = document.getElementById("pruebaj");
    element.classList.add("mystyle");
  }

  function scrollWin() {
    window.scrollTo(0, 0);
  }
</script>

<style>
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
  @media only screen and (max-width: 950px) {
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

  <div class="container tiendas" id="about">

    <h1>¿QUÉ ES?</h1>
    <hr />
    <h4>UNIGO:</h4>
    <p>
      Esta iniciativa y modelo de negocio nace de la necesidad de los
      compradores y visitantes del mall; porque muchas personas tienen temor de
      visitar libremente el centro comercial en estos momentos de crisis
      sanitaria; La tendencia actual nos invita a utilizar las compras en línea
      y el uso del delivery ya que las cifras nacionales nos demuestran que el
      servicio a incrementado un 30% más que el año pasado.
      <br />
      <br />
      - Es por ello que se crea UNIGO, un portal digital en nuestra página Web,
      en donde tu podrás visitarnos y realizar tus compras de una manera fácil y
      segura desde la comodidad de tú casa e ir a traer tus productos en las
      zonas UNIGO establecidas.
    </p>
    <br />
    <br />

    <h4>Objetivos:</h4>
    <p>
      Incrementar las ventas de nuestros socios comerciales Incrementar las
      visitas al mall en estas zonas de entrega, potenciar la marca, y que poco
      a poco vayan generando confianza para realizar visitas presenciales. Crear
      espacios seguros y señalizados para la entrega eficiente de los productos
      de los inquilino y propietarios del mall, cumpliendo con las medidas de
      bioseguridad.
    </p>
    <br />

    <div id="howto" />
    <h1>¿Cómo funciona?</h1>
    <hr />
    <p>
      <strong>Paso No. 1:</strong>
      <br />
      El cliente ingresa a:
      <br />
      www.malluniplaza.com/unimall-choluteca/UNIGO
      <br />
      <br />
      <strong>Paso No. 2:</strong>
      <br />
      Escoge tu tienda favorita, revisa los productos y contacta al número de la
      tienda para realizar tu pedido.
      <br />
      <br />
      <strong>Paso No. 3:</strong>
      <br />
      Visita Unimall dirígete al área señalizada de UNIGO en cualquier de
      nuestras zonas establecidas en el estacionamiento.
      <br />
      <br />
      <strong>Paso No. 4:</strong>
      <br />
      El cliente avisa a la tienda que ya está en el punto de entrega para que
      le lleven su compra.
      <br />
      <br />
      <strong>Paso No. 5:</strong>
      <br />
      El cliente se comunica con la tienda para coordinar la entrega de su
      compra.
    </p>

  </div>

  <div class="container tiendas" id="ubicaciones">
    <h1>Ubicaciones</h1>
    <img src="/img/plano.jpg" alt="plano" width="100%" />

  </div>
  <br />
  <br />

  <div class="container aligncenter bodycontent">
    {#each data as item}
      <GridStores
        store={item.title.rendered}
        image={item.better_featured_image.source_url}
        url={item.slug}
        fblink={item.acf.link_de_instagram}
        iglink={item.acf.link_de_facebook}
        walink={item.acf.numero_whatsapp}
        linkwebsite={item.acf.link_website}
        linkcatalogo={item.acf.link_del_catalogo}
        zonamall={item.acf.zonamall} />
    {:else}
      <div class="preloader">
        <img alt="loading" src="./img/loading.gif" />
      </div>
    {/each}
  </div>

</main>
<Footer />
