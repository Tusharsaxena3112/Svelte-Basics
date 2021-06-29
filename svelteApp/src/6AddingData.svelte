<script>
  let persons = [];
  let name;
  let about;
  let professional;

  const addItem = () => {
    persons = [
      ...persons,
      {
        name,
        about,
        professional,
      },
    ];
  };
</script>

<main>
  <h1>Adding User Input</h1>
  <input type="text" bind:value={name} />
  <input type="text" bind:value={about} />
  <input type="text" bind:value={professional} />
  <button on:click={addItem}>Add item</button>
  <div class="persons">
    {#each persons as person}
      <div class="person">
        <h1>{person.name}</h1>
        <p>{person.about}</p>
        <h2>{person.professional}</h2>
      </div>
    {/each}
  </div>
</main>

<style>
  .persons {
    display: grid;
    grid-template-columns: auto auto auto auto auto;
    justify-content: center;
    align-items: center;
  }
  .person {
    border: 1px solid white;
    background-color: black;
    color: white;
    margin: 10px;
    box-shadow: 1px 1px 2px 2px grey;
  }
  p {
    padding: 5px;
  }
</style>
