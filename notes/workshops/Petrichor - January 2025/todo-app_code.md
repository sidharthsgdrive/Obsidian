<script>
	let todos = [{
		text: "Todo",
		done: false
	}]
</script>

<form onsubmit={(e) => {
	e.preventDefault()
	console.log("Hello")
}}>
							 

	<input placeholder = "Enter todo">
</form>

<br>

{#each todos as todo}
	{#if !todo.done}
	<input type="checkbox" onchange={()=>{todo.done = !todo.done}} > {todo.text}
	{/if}
{/each}

<p>Done todos</p>
{#each todos as todo}
	{#if todo.done}
	<input type="checkbox" onchange={()=>{todo.done = !todo.done}} > {todo.text}
	{/if}
{/each}