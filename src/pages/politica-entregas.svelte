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
  .image {
    width: 60%;
    margin: 0 auto;
  }
</style>

<Header />
<div class="container tiendas">

  <h1>Politica de Entregas (pick up)</h1>
  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>
  <div class="image">
    <img src="./img/entregas.jpg" alt="unimall delivery" width="100%" />
  </div>
  <br />

  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>

  <p>
    Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod
    tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
    quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
    consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
    cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat
    non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
  </p>

</div>
<Footer />
