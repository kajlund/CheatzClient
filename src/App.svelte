<script>
  import { Router, Route, navigate } from "svelte-navigator"
  import AppHeader from "./components/AppHeader.svelte";
  import SideBar from "./components/SideBar.svelte"

  import Home from "./pages/Home.svelte"
  import About from "./pages/About.svelte"

  let open = false

  function menuAction(event) {
    // open = !open;
    console.log('App menuAction: ', event.detail)
    switch (event.detail) {
      case 'home':
        navigate('/')
        break
    }
  }

  const sideBarSelection = (e) => {
    console.log('sideBarSelection: ', e.detail)
    open = false;
    switch (e.detail) {
      case 'home':
        navigate('/')
        break
      case 'about':
        navigate('/about')
        break
    }
  }
</script>

<Router>
  <AppHeader bind:open={open} on:menu-action={menuAction} />
  <SideBar bind:open on:sidebar-selection={sideBarSelection} />
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
    padding: 0 1rem;
    margin-top: 86px;
  }

  @media screen and (min-width: 768px) {
    main {
      max-width: 900px;
      margin-left: auto;
      margin-right: auto;
    }
  }
</style>
