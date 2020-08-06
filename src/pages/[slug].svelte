<script>
  import { params } from "@sveltech/routify";
  import Header from "../components/header.svelte";
  import Footer from "../components/footer.svelte";
  import SingleStore from "../components/singleStore.svelte";
  import { onMount } from "svelte";

  console.log($params);

  let slug = $params;

  console.log(slug.slug);

  const apiURL = `https://www.malluniplaza.com/wp-json/wp/v2/tiendasunigo?slug=${slug.slug}`;
  let data = [];

  onMount(async function () {
    const response = await fetch(apiURL);
    data = await response.json();
    console.log(data);
  });
</script>

<style>
  .tiendas {
    margin-top: 0px;
    border: 1px dotted #ccc;
    padding: 15px;
  }
  .image {
    top: 15px;
    vertical-align: top;
    display: inline-block;
    width: 30%;
    overflow: auto;
    height: auto;
  }
  .content {
    display: inline-block;
    width: 60%;
    vertical-align: top;
    height: 100%;
    margin-left: 60px;
  }
  .content h1 {
    text-align: center;
    font-size: 26px;
    color: #153252;
    font-weight: 600;
    font-family: Roboto;
    text-decoration: underline;
    text-transform: capitalize;
    letter-spacing: 1px;
  }
  .content p {
    color: #153252;
    font-family: Roboto;
  }
  .preloader {
    width: 100%;
    text-align: center;
    margin: 0 auto;
  }
  .socialmedia h3 {
    font-size: 16px;
    font-weight: 600;
  }
  .catalogoLink h3 {
    font-size: 16px;
    font-weight: 600;
    margin-bottom: 15px;
  }

  .catalogoLink a {
    width: 190px;
    height: 30px;
    background: #f9b218;
    border-radius: 4px;
    padding: 9px;
    text-align: center;
    color: #153252;
    font-weight: 800;
    font-family: Roboto;
    margin-top: 10px;
  }

  .categoria h3 {
    margin-top: 15px;
    text-align: center;
    font-size: 18px;
    color: #153252;
    font-weight: 300;
    font-family: Roboto;
  }

  .categoria span {
    font-weight: 600;
  }

  @media only screen and (max-width: 950px) {
    .tiendas {
      margin-top: -20px;
      border: 1px dotted #ccc;
      padding: 15px;
    }
    .image {
      display: block;
      width: 100%;
      overflow: auto;
      height: auto;
    }
    .content {
      display: block;
      width: 100%;
      height: auto;
      margin-left: 0px;
    }
  }
</style>

<Header />
<br />
<br />

{#each data as item}
  <div class="container tiendas">
    <div class="image">
      <img
        src={item.better_featured_image.source_url}
        alt="logo"
        width="100%" />
      <div class="categoria">
        <h3>
          <span>Categoria:</span>
          {item.categoria}
        </h3>
      </div>
    </div>
    <div class="content">
      <h1>{item.title.rendered}</h1>
      <p>
        {@html item.content.rendered}
      </p>

      <div class="socialmedia">
        <h3>Visita Nuestras Redes Sociales</h3>
        <a href={item.link_de_facebook} target="_blank">
          <img src="./img/fbstore.png" alt={item.title.rendered} />
        </a>
        <a href={item.acf.link_de_instagram} target="_blank">
          <img src="./img/igstore.png" alt={item.title.rendered} />
        </a>
        <a href="https://wa.me/{item.acf.numero_whatsapp}" target="_blank">
          <img src="./img/wastore.png" alt={item.title.rendered} />
        </a>
        <a href={item.acf.link_website} target="_blank">
          <img src="./img/website.png" alt={item.title.rendered} />
        </a>
      </div>

      <div class="catalogoLink">
        <h3>Revisa Nuestro Catalogo</h3>
        <a href={item.link_del_catalogo} target="_blank">Ver Catalogo</a>
      </div>

    </div>
  </div>
{:else}
  <div class="preloader">
    <img alt="loading" src="./img/loading.gif" />
  </div>
{/each}

<Footer />
