<script>
  import Header from "../components/header.svelte";
  import Footer from "../components/footer.svelte";
</script>

<style>
  .tiendas {
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

<svelte:head>
  <title>Ubicaciones - Unigo</title>
  <meta name="description" content="Encuentra nuestra ubicación fácilmente" />
</svelte:head>

<Header />
<div class="container tiendas">

  <h1>Plano</h1>
  <p>
    <strong>Proximamente...</strong>
    <br />

  </p>

</div>
<Footer />
