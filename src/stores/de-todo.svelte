<script context="module">
  export async function preload({ paramns, query }) {
    const res = await this.fetch(
      `http://www.malluniplaza.com/wp-json/wp/v2/tiendasunigo?slug=${params.slug}`
    );

    const data = await res.json();

    return { post: data[0] };
  }

  export let post;
  console.log(posts);
</script>
