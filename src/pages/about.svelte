<script>
  import Header from "../components/header.svelte";
  import Footer from "../components/footer.svelte";
</script>

<style>
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
</style>

<Header />
<div class="container tiendas">

  <h1>¿QUÉ ES?</h1>
  <h4>UNIGO:</h4>
  <p>
    Esta iniciativa y modelo de negocio nace de la necesidad de los compradores
    y visitantes del mall; porque muchas personas tienen temor de visitar
    libremente el centro comercial en estos momentos de crisis sanitaria; La
    tendencia actual nos invita a utilizar las compras en línea y el uso del
    delivery ya que las cifras nacionales nos demuestran que el servicio a
    incrementado un 30% más que el año pasado.
    <br />
    <br />
    - Es por ello que se crea UNIGO, un portal digital en nuestra página Web, en
    donde tu podrás visitarnos y realizar tus compras de una manera fácil y
    segura desde la comodidad de tú casa e ir a traer tus productos en las zonas
    UNIGO establecidas.
  </p>
  <br />

  <h4>Objetivos:</h4>
  <p>
    Incrementar las ventas de nuestros socios comerciales Incrementar las
    visitas al mall en estas zonas de entrega, potenciar la marca, y que poco a
    poco vayan generando confianza para realizar visitas presenciales. Crear
    espacios seguros y señalizados para la entrega eficiente de los productos de
    los inquilino y propietarios del mall, cumpliendo con las medidas de
    bioseguridad.
  </p>

</div>
<Footer />
