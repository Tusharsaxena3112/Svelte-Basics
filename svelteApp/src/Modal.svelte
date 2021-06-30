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
    background-color: rgb(36, 23, 23);
    width: 99%;
    height: 99%;
    position: fixed;
    color: white;
    margin:0;
  }
</style>
