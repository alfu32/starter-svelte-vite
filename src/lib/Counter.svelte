<script>

	import { count } from '../store/store.js';

function decrement() {
  count.update(n => n - 1);
}
  const increment = () => {
    count.update(n => n + 1);
  }
</script>

<button on:click={increment}>
  ++
</button>
<button on:click={decrement}>
  --
</button>
<pre>count is {count}</pre>
  
  