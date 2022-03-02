<script>
  const pelis = [
    { name: "matrix 1", available: 2, quantity: 0 },
    { name: "matrix 2", available: 1, quantity: 0 },
    { name: "matrix 3", available: 5, quantity: 0 }
  ];
</script>

{#each pelis as movie}
<form>
	<h3>{movie.name}</h3>
	<button type="button" on:click={() => movie.quantity -=1} disabled={movie.quantity===0}>-</button>
	{movie.quantity}
	<button type="button" on:click={() => movie.quantity +=1} disabled={movie.quantity===movie.available}>+</button>
</form>
{/each}