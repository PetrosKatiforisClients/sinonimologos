<script>
  export let label
</script>

<button on:click>
  { label }
</button>

<style>
  button {
    background-color: var(--bg-lighter);
    padding: 0.4em 1em;

    border: none;
    color: white;
    border-radius: var(--radius);

    cursor: pointer;
  }

  @media (max-width: 30em) {
    button {
      font-size: 0.75rem;
    }
  }
</style>
