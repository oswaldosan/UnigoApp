<script context="module">
  import { fade } from "svelte/transition";
  import { fly } from "svelte/transition";
  import { quintOut } from "svelte/easing";
</script>

<style>
  .container {
    padding-top: 45px;
  }

  .text {
    font-family: "Roboto";
    color: #153252;
    text-transform: uppercase;
    background-image: url("/img/gobg.png");
    background-size: contain;
    background-repeat: no-repeat;
    height: 500px;
    padding-top: 150px;
    padding-left: 0px;
    background-position: center;
    text-align: center;
  }

  .haztus {
    font-family: "Montserrat";
    color: #153252;
    font-weight: 500;
    font-size: 49px;
    margin-bottom: -30px;
  }
  .compras {
    font-family: "Montserrat";
    font-weight: 900;
    font-size: 73px;
    margin-bottom: -15px;
  }

  .bajar {
    font-family: "Montserrat";
    font-size: 28px;
    font-weight: 600;
  }
  .divider {
    width: 100%;
    z-index: 9999;
  }
  .slider {
    text-align: left;
  }

  @media only screen and (max-width: 950px) {
    .compras {
      font-size: 63px;
    }
    .slider {
      text-align: center;
    }
    .text {
      font-family: "Roboto";
      color: #153252;
      text-transform: uppercase;
      background-image: url("/img/gobg.png");
      background-size: contain;
      background-repeat: no-repeat;
      height: 300px;
      padding-top: 50px;
      padding-left: 0px;
      background-position: center;
      text-align: center;
    }
    .car {
      display: none;
    }
  }
</style>

<div class="container">
  <div class="row align-items-center slider">
    <div
      class="col-7 car"
      transition:fly={{ delay: 50, duration: 600, x: -1500, y: 10, opacity: 0.1, easing: quintOut }}>
      <img alt="slider Car unigo" src="./img/headcar.png" width="100%" />
    </div>
    <div
      class="col text"
      transition:fly={{ delay: 50, duration: 600, x: 1500, y: 10, opacity: 0.1, easing: quintOut }}>
      <div class="haztus">Haz tus</div>
      <div class="compras">Compras</div>
      <div class="bajar">Sin bajar de tu auto</div>
    </div>
  </div>
</div>

<div class="divider">
  <img alt="slider Car unigo" src="./img/sectiondivider.jpg" width="100%" />
</div>
