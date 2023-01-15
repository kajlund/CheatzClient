<script>
  import {Router, Route } from "svelte-navigator"
  import Header from "./components/Header.svelte"
  import Home from "./pages/Home.svelte"
  import About from "./pages/About.svelte"
</script>

<Router>
  <Header />
  <main>
    <Route>
      <Home />
    </Route>
    <Route path="about">
      <About />
    </Route>
  </main>
</Router>

<style>
  main {
    max-width: 800px;
    margin: 0 auto;
    margin-top: 86px;
  }
</style>
