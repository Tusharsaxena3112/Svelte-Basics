<script>
  export let showModel;
</script>

<main>
  {#if showModel}
  <h1>Enter your Details</h1>
    <div class="model">
      <input type="text" />
      <input type="text" />
      <input type="text" />
      <button on:click|self>Add item</button>
    </div>
  {/if}
</main>

<style>
    .model{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    h1{
        text-align: center;
    }
    input{
        margin:5px;
    }
    button{
        margin:5px;
    }
  main {
    background-color: rgb(0, 0, 0);
    width: 100vw;
    height: 100vh;
    position: fixed;
    color: white;
  }
</style>
