<script>
  import Modal from "./Modal.svelte";
    let persons = [];
    let name;
    let about;
    let professional;
    let showModel = false;

    const handleShow = () =>{
      showModel = !showModel;
    }
  
    const addItem = () => {
      persons = [
        ...persons,
        { id:persons.length +1,  
          name,
          about,
          professional,
        },
      ];
      handleShow();
    };

    const deleteItems = (personId) =>{
        persons = persons.filter((person) =>{
            return person.id!== personId;
        });
    }
  </script>
  
  <main>
    <!-- <h1>Adding User Input</h1>
    <input type="text" bind:value={name} />
    <input type="text" bind:value={about} />
    <input type="text" bind:value={professional} />
    <button on:click={addItem}>Add item</button> -->
    {#if showModel}
    <Modal on:click={addItem} {showModel}/>
    {/if}
    <button on:click={handleShow}>Enter</button>
    <div class="persons">
    
      {#each persons as person}
        <div class="person">
          <h1>{person.name}</h1>
          <p>{person.about}</p>
          <h2>{person.professional}</h2>
          <button on:click={()=>deleteItems(person.id)}>Delete</button>
        </div>
      {/each}
    </div>
  </main>
  
  <style>
    .persons {
      display: grid;
      grid-template-columns: auto auto auto auto auto;
      justify-content: center;
      align-items: center;

    }
    .person {
      border: 1px solid white;
      background-color: black;
      color: white;
      margin: 10px;
      box-shadow: 1px 1px 2px 2px grey;
    }
    p {
      padding: 5px;
    }
  </style>
  