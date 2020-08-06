<script>
  export let storeTitle;
  export let storelogo;
  export let description;
</script>

<style>
  .title {
    position: relative;
    font-size: 24px;
    font-weight: 600;
    text-align: center;
    width: 300px;
    margin: 0 auto;
    margin-top: 20px;
  }

  .storelogo {
    border-radius: 4px;
  }
  .container {
    margin-top: 20px;
    border: 1px solid #ccc;
  }
  .goback {
    width: 28px;
    position: absolute;
    left: 60px;
    top: -3px;
  }

  .goback img {
    width: 100%;
  }

  @media only screen and (max-width: 950px) {
    .goback {
      margin-top: 5px;
      margin-left: 50px;
    }
  }
</style>

<div class="title">
  <a href="/">
    <div class="goback">
      <img src="./undo.svg" alt="back" />
    </div>
  </a>
  {storeTitle}
</div>

<div class="container">
  <div class="contenedormid">
    <div class="storelogo">
      <img src={storelogo} alt="logo" />
    </div>
  </div>
  <div class="contenedormid2">
    {@html description}
  </div>

</div>
