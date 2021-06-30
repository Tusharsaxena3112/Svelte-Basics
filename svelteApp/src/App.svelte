<script>
  import Todo from "./TodoApp.svelte";
</script>

<main>  
  <Todo/>
</main>

<style>
  * {
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }
  @media (min-width: 640px) {
    main {
      max-width: none;
    }
  }
</style>
