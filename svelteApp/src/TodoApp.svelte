<script>
  import InputModel from "./InputModel.svelte";
  let tasks = [];
  let sr;
  let task;
  let status;
  let showModel = false;

  const toggle = () => {
    showModel = !showModel;
  };
  const addTask = (e) => {
    sr = tasks.length+1;
    task = e.detail.task;
    status = e.detail.status;
    tasks = [...tasks, { sr, task, status }];
    toggle();
  };

  const deleteTask = (sr) =>{
      tasks = tasks.filter(task=>{
          return sr!=task.sr;
      })
  }
</script>

<main>
  {#if showModel}
    <InputModel on:data={addTask} on:click={toggle} />
  {/if}
  <h1>Todo App</h1>
  <table>
    <tr>
      <th>Sr no.</th>
      <th>Task</th>
      <th>Status</th>
      <th> <button on:click={toggle}>Add task to your Todo's</button></th>
    </tr>
    {#each tasks as task}
      `<tr
        ><td>{task.sr}</td><td>{task.task}</td><td>{task.status}</td><td
          ><button on:click={()=>deleteTask(task.sr)}>Delete</button>
          </td
        ></tr
      >`
    {/each}
  </table>
</main>

<style>
  h1 {
    text-align: center;
  }
  table {
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    border: 1px solid black;
    border-collapse: collapse;
  }
  th {
    border: 1px solid black;
    border-collapse: collapse;
  }

  td,
  th,
  tr {
    padding: 30px;
    font-size: 20px;
  }
  button{
      margin: 0 auto;
  }
</style>
