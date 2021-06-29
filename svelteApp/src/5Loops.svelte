<script>
  let persons = [
    {
      name: "Tushar Saxena",
      professional: "Developer",
      about: "hhhiwghrgjwrbuh3iroqklwwww,vdm,vbbdbkughirorwklnmf",
    },
    {
      name: "Tanishq Saxena",
      professional: "Student",
      about: "hhhiwghrgjwrbuh3iroqklwwww,vdm,vbbdbkughirorwklnmf",
    },
    {
      name: "Pavit Saxena",
      professional: "Student",
      about: "hhhiwghrgjwrbuh3iroqklwwww,vdm,vbbdbkughirorwklnmf",
    },
  ];
</script>

<main>
  <h1>Loops in Svelte!</h1>
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
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .person {
    border: 1px solid white;
    background-color: black;
    color:white;
    margin:10px;
    box-shadow: 1px 1px 2px 2px grey;
  }
  p{
      padding:5px;
  }
</style>
