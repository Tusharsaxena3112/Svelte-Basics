<script>
    let count = 0;

    const increaseCount = () =>{
        count+=1;
    }
</script>

<main>
    <h1>1. Basics of Svelte (Counter)</h1>
    <h1>Count:{count}</h1>
    <button on:click={increaseCount}>Click</button>
</main>

<style>

</style>