<script>
  export let label

  import Dropdown from "$lib/components/Dropdown.svelte"
  import MenuButton from "$lib/components/Menu/MenuButton.svelte"

  // Dropdown state management
  let isOpen = false

  function toggleIsOpen() {
    isOpen = !isOpen
  }
</script>

<div>
  <MenuButton {label} on:click={toggleIsOpen} />

  <Dropdown {isOpen} {toggleIsOpen} width={300}>
    <div class="dropdown__content">
      <slot />
    </div>
  </Dropdown>
</div>

<style>
  .dropdown__content {
    padding: 0.7em 1em;
  }
</style>
