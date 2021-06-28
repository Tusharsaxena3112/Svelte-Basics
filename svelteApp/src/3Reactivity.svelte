<script>
    let firstName="";
    let lastName="";
    $:fullName = `${firstName} ${lastName}` //Reactive Values
    // $:console.log(`${fullName}`); // Reactive Statement
    $:{
        console.log(`${firstName}`);
        console.log(`${lastName}`);
        console.log(`${fullName}`);
    } // Reactive Block
</script>

<main>
    <h1>Reactivity in SvelteJS</h1>
    <input type="text" bind:value={firstName}>
    <input type="text" bind:value={lastName}>
    <h1>{fullName}</h1>
</main>

<style>

</style>