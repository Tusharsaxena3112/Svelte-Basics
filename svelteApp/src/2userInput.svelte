<script>
    let firstName ;
    let lastName;
    let fullName ;
    const handleInput = () =>{
        fullName = `${firstName} ${lastName}`;
    }
</script>

<main>
    <h1>Handling User Input and Data Binding</h1>
    <input type="text" bind:value={firstName}>
    <input type="text" bind:value={lastName}>
    <h1>{fullName}</h1>
    <button on:click={handleInput}>Click</button>
</main>

<style>

</style>