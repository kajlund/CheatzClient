<script>
  import {Link} from "svelte-navigator"
</script>

<div class="wrap">
  <a href="/">
    <span class="material-symbols-rounded">
      map
    </span>
    <h1 class="app-title">Cheatz v2</h1>
  </a>
</div>

<style>
  .wrap {
    display: flex;
    align-items: center;
  }
  .wrap a {
    display: flex;
    color: var(--col-primary);
  }
  .app-title {
    color: var(--primary-color);
  }

  h1 {
    font-size: 2rem;
    margin-top: 0.4rem;
  }
  span {
    margin-left: 1rem;
    font-size: 3rem;
  }
</style>