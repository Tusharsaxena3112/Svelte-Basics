<script>
    export let name;
    export let age;
    export let gender;
    export let martialStatus;
</script>

<main>
<h1>Props in Svelte!</h1>
<ul>
    <li>{name}</li>
    <li>{age}</li>
    <li>{gender}</li>
    <li>{martialStatus}</li>
</ul>
</main>

<style>
    ul{
        list-style: none;
    }
    li{
        background-color: yellow;
        color: red;
        margin:10px;
    }
</style>