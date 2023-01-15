<script>
  import { createEventDispatcher } from "svelte"

  import Burger from "./Burger.svelte"
  import Logo from "./Logo.svelte"

  export let open = false

  const dispatch = createEventDispatcher()

  function toggleBurger(event) {
    // open = !open;
    console.log(event.detail)
  }
</script>

<nav>
  <Burger bind:open on:burger-toggle={toggleBurger} />
  <Logo />
</nav>

<style>
  nav {
    display: flex;
  }
</style>