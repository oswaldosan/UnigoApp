<script>
  import GridStores from "./gridstores.svelte";
  import { onMount } from "svelte";

  const apiURL =
    "https://www.malluniplaza.com/wp-json/wp/v2/tiendasunigo?zona=37&per_page=30";
  let data = [];

  onMount(async function () {
    const response = await fetch(apiURL);
    data = await response.json();
    console.log(data);
  });
</script>

<div class="aligncenter">
  {#each data as item}
    <GridStores
      store={item.acf.nombre_de_la_tienda}
      image={item.acf.logo_de_la_tienda}
      url={item.slug}
      fblink={item.acf.link_de_instagram}
      iglink={item.acf.link_de_facebook}
      walink={item.acf.numero_whatsapp}
      linkwebsite={item.acf.link_website}
      linkcatalogo={item.acf.link_del_catalogo}
      zonamall={item.acf.zonamall} />
  {:else}
    <div class="preloader"><img alt="loading" src="./img/loading.gif" /></div>
  {/each}
</div>
