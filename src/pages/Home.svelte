<script>
  import Carousel from "svelte-carousel"

  import Img01 from "../img/geo01.jpg"
  import Img02 from "../img/geo02.jpg"
  import Img03 from "../img/geo03.jpg"
  import Img04 from "../img/geo04.jpg"
  import Img05 from "../img/geo05.jpg"

  let carousel
</script>
<h1>
  <span class="material-symbols-rounded">construction</span>
  Under construction...
</h1>
<Carousel bind:this={carousel} pauseOnFocus="true" autoplay="true">
  <div>
    <img src="{Img01}" alt="Geo01">
  </div>
  <div>
    <img src="{Img02}" alt="Geo02">s
  </div>
  <div>
    <img src="{Img03}" alt="Geo03">
  </div>
  <div>
    <img src="{Img04}" alt="Geo04">
  </div>
  <div>
    <img src="{Img05}" alt="Geo05">
  </div>
</Carousel>

<style>
  span {
    font-size: 3.5rem;
  }
  img {
    opacity: 0.8;
    border: 5px solid #333;
  }
</style>
