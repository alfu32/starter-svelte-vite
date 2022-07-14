<script>

	import { counterStore} from '../store/store.js';

  function decrement() {
    counterStore.update(counters => {
      counters[name] = (counters[name]||0)-1;
      return {...counters};
    });
  }
  const increment = () => {
    counterStore.update(counters => {
      counters[name] = (counters[name]||0)+1;
      return {...counters};
    });
  }
  export let name="counter";
  let countValue;

	counterStore.subscribe(counters => {
		countValue = (counters[name]||0);
	});
</script>

<button on:click={decrement}>
  &lt;
</button>
<span style="display:inline-block">[{name}]={countValue}</span>
<button on:click={increment}>
  &gt;
</button>

  
  