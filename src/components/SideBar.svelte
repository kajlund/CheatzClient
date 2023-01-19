<script>
  import { createEventDispatcher } from "svelte"

  import SidebarItem from "./SidebarItem.svelte"

  export let open = false
  const dispatch = createEventDispatcher()
</script>

<aside class={open ? 'open' : ''}>
  <nav>
    <ul>
      <li>
        <SidebarItem
          caption="Home"
          icon="home"
          on:click={() => dispatch('sidebar-selection', 'home')} />
      </li>
      <li>
        <SidebarItem
          caption="Public Caches"
          icon="location_on"
          on:click={() => dispatch('sidebar-selection', 'public')} />
      </li>
      <li>
        <SidebarItem
          caption="Private Caches"
          icon="location_off"
          on:click={() => dispatch('sidebar-selection', 'private')} />
      </li>
      <li>
        <SidebarItem
          caption="Municipalities"
          icon="satellite"
          on:click={() => dispatch('sidebar-selection', 'municipalities')} />
      </li>
      <li class="divider" />
      <li>
        <SidebarItem
          caption="About"
          icon="info"
          on:click={() => dispatch('sidebar-selection', 'about')} />
      </li>
      <li class="divider" />
      <li>
        <SidebarItem
          caption="Login"
          icon="login"
          on:click={() => dispatch('sidebar-selection', 'login')} />
      </li>
      <li>
        <SidebarItem
          caption="Logout"
          icon="logout"
          on:click={() => dispatch('sidebar-selection', 'logout')} />
      </li>
      <li>
        <SidebarItem
          caption="Profile"
          icon="settings_account_box"
          on:click={() => dispatch('sidebar-selection', 'profile')} />
      </li>
    </ul>
  </nav>
</aside>

<style>
  aside {
    z-index: 2;
    position: fixed;
    left: -100%; /* offscreen by default */
    top: 58px;
    width: 70%;
    /* height: 65vh; */
    transition: left 0.5s ease-in-out;
    background: #fff;
    border: 1px solid #eee;
    border-radius: 0.5rem;
    box-shadow: 1px 1px 8px rgba(77, 51, 51, 0.26);
    padding: 0.5rem;
  }

  ul {
    margin: 0;
    padding: 0;
    list-style-type: none;
  }

  .open {
    left: 0; /* slide on screen */
  }
  .divider {
    border-top: 1px solid #eee;
    margin: 4px 0;
  }

  @media screen and (min-width: 768px) {
  aside {
    width: 30%;
    max-width: 20rem;
  }
}
</style>
