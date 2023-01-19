<script>
  import Burger from "./Burger.svelte";
  import Logo from "./Logo.svelte";

  export let open = false;
</script>

<header>
  <nav>
    <Burger bind:open />
    <Logo />
  </nav>
</header>

<style>
  header {
    position: fixed;
    display: flex;
    top: 0;
    left: 0;
    width: 100%;
    padding: 0.5rem;
    color: #666;
    background: whitesmoke;
    box-shadow: 0 2px 6px rgba(0, 0, 0, 0.26);
  }

  nav {
    display: flex;
    align-items: center;
    height: 40px;
  }
</style>
