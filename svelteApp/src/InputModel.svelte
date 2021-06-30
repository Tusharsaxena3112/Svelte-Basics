<script>
  let task;
  let status;

  import { createEventDispatcher } from "svelte";
  let dispatch = createEventDispatcher();
  const handleSubmit = () => {
    const data = {
      task,
      status,
    };
    // console.log(data);
    dispatch("data", data);
  };
</script>

<main>
  <div class="background" on:click|self>
    <h1>Add your task!</h1>
    <div class="inputs">
      <form on:submit|preventDefault={handleSubmit}>
      <input type="text" bind:value={task} placeholder="task"/>
      <input type="text" bind:value={status} placeholder="status"/>
      <button type="submit">Add!</button>
      <form/>
    </div>
  </div>
</main>

<style>
  h1 {
    color: white;
    text-align: center;
  }
  .background {
    background-color: black;
    width: 99%;
    height: 99%;
    position: fixed;
    display: flex;
    flex-direction: column;
  }
  .inputs {
    background-color: blanchedalmond;
    padding: 10px;
    width:50%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    border-radius: 10px;
    margin:0 auto;
  }
  input{
      margin:10px;
      padding:10px;
      border:none;
      outline:none;
      border-radius: 2px;
  }
</style>
