<script>
  export let caption = "Item";
  export let enabled = true;
  export let icon = null;

</script>

<button on:click class={enabled ? '' : 'disabled'} disabled={!enabled}>
  <span class="material-symbols-rounded icon">{icon}</span>
  {caption}
</button>

<style>
  button {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: flex-start;
    padding: 0.5rem 1rem;
    background-color: transparent;
    border: none;
    outline: transparent;
    color: #999;
    font-size: 1.2rem;
    margin: 0;
    text-decoration: none;
  }
  button:hover {
    background: #eee;
    color: #666;
  }
  .disabled {
    color: #eee;
    cursor: not-allowed;
  }
  .icon {
    margin-right: 4px;
  }
</style>