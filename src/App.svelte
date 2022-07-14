<script>
  import Counter from './lib/Counter.svelte'

  let counters=[
    "cats","dogs","poneys","rabbits","puppies","unicorns",
  ];
  function addItem(){
    counters=[...counters,`another-${counters.length}`];
  }
</script>

<main>
  <h1>Magic Inventory</h1>
  {#each counters as counterName}
    <Counter name={counterName}/><br/>
  {/each}
  <button on:click={addItem}>add item</button>
</main>