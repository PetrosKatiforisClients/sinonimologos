<script>
  import DropdownButton from "$lib/components/Menu/DropdownButton.svelte" 
  import MenuButton from "$lib/components/Menu/MenuButton.svelte"

  import { synonym } from "$lib/stores/synonymsStore.js"
  import dictionary from "$lib/data/dictionary.js"

  // Picking a random word from the synonyms dictionary
  function randomWord() {
    let randomIndex = Math.floor(Math.random() * (Object.keys(dictionary).length - 1))

    synonym.set(Object.keys(dictionary)[randomIndex])
  }
</script>

<div class="menu__buttons">
  <DropdownButton label="Πώς Δημιουργήθηκε">
    <p>Η ιστοσελίδα δημιουργήθηκε χρησιμοποιώντας την Svelte.js</p>
    
    <p>Ο κώδικας είναι δημοσίως διαθέσιμος 
      <a target="_blank" href="https://github.com/PetrosKatiforisClients/sinonimologos">εδώ</a>
    </p>
  </DropdownButton>

  <DropdownButton label="Επικοινωνία">
    <p>
      Για οποιαδήποτε ερώτηση μπορείτε να επικοινωνήσετε
      μέσω email εδώ: pkatif@mail.com
    </p>
  </DropdownButton>

  <MenuButton label="Τυχαία Λέξη" on:click={randomWord} />
</div>

<style>
  .menu__buttons {
    display: flex;
    align-items: center;
    justify-content: center;

    gap: 1em;
  }

  @media (max-width: 35em) {
    .menu__buttons {
      gap: 0.5em;

      flex-direction: column;
      align-items: flex-start;
    }
  }
</style>
