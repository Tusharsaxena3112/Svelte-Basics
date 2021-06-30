<script>
  export let showModel;
  export let name;
  export let about;
  export let professional;
</script>

<main>
  {#if showModel}
    <h1>Enter your Details</h1>
    <div class="model">
      <input type="text" bind:value={name}/>
      <input type="text" bind:value={about}/>
      <input type="text" bind:value={professional}/>
      <button on:click|self>Add item</button>
    </div>
  {/if}
</main>

<style>
  .model {
    display: flex;
    justify-content: center;
    align-items: center;
  }
  h1 {
    text-align: center;
  }
  input {
    margin: 5px;
  }
  button {
    margin: 5px;
  }
  main {
    background-color: rgb(36, 23, 23);
    width: 99%;
    height: 99%;
    position: fixed;
    color: white;
    margin: 0;
  }
</style>
