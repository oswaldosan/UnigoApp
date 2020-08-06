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
  .image {
    width: 60%;
    margin: 0 auto;
  }
</style>

<Header />
<div class="container tiendas">

  <h1>¿Cómo funciona?</h1>
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
    Visita Unimall dirígete al área señalizada de UNIGO en cualquier de nuestras
    zonas establecidas en el estacionamiento.
    <br />
    <br />
    <strong>Paso No. 4:</strong>
    <br />
    El cliente avisa a la tienda que ya está en el punto de entrega para que le
    lleven su compra.
    <br />
    <br />
    <strong>Paso No. 5:</strong>
    <br />
    El cliente se comunica con la tienda para coordinar la entrega de su compra.
  </p>
  <div class="image">
    <img src="./img/bioseguridad.jpg" alt="unimall delivery" width="100%" />
  </div>
  <br />

</div>
<Footer />
