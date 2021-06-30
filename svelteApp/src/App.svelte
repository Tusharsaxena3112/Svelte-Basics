<script>
  // import Basics from "./1basics.svelte";
  // import UserInput from "./2userInput.svelte";
  // import Reactivity from "./3Reactivity.svelte";
  // import Props from "./4Props.svelte";
  // import Loops from "./5Loops.svelte";
  // import AddItem from "./6AddingData.svelte";
  import DeletetingItem from "./DeletetingItem.svelte";
  // import DeleteItem from "./DeletetingItem.svelte";
  const props = {
    name: "Tushar",
    age: 21,
    gender: "male",
    martialStatus: "single",
  };
</script>

<main>
  <!-- <Basics/> -->
  <!-- <UserInput/> -->
  <!-- <Reactivity/> -->
  <!-- <Props {...props}/> -->
  <!-- <Loops/> -->
  <!-- <AddItem/> -->
  <DeletetingItem />
</main>

<style>
 


  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
