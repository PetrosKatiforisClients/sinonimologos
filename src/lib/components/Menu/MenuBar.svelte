<script>
  import FavouritesButton from "$lib/components/Menu/FavouritesButton.svelte"
  import MenuButtons from "$lib/components/Menu/MenuButtons.svelte"
</script>

<div id="menubar">
  <MenuButtons />

  <FavouritesButton />
</div>

<style>
  #menubar {
    display: flex;
    
    align-items: center;
    justify-content: space-between;

    margin-bottom: 6em;
    gap: 1em;

    padding: 0 var(--padding-x);
  }

  @media (max-width: 35em) {
    #menubar {
      align-items: flex-start;
      justify-content: flex-start;

      flex-direction: column;

      margin-bottom: 5em;
    }
  }
</style>
