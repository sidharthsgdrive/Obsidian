<script>
	let todos = []
	let todo_box = ""
</script>

<form onsubmit={(e) => {
	e.preventDefault()
	// another way to push elements
	todos = [...todos, {
		text: todo_box,
		done: false
	}]
	todo_box = ""
}}>
							 

	<input placeholder = "Enter todo"
		bind:value={todo_box}>
	{todo_box}
</form>

<br>

<u>Unfinished tasks:</u>
{#each todos as todo}
	{#if !todo.done}
	<input type="checkbox" onchange={()=>{todo.done = !todo.done}} > {todo.text}
	{/if}
{/each}

<br>
<br>

<u>Finished tasks:</u>
{#each todos as todo}
	{#if todo.done}
	<input type="checkbox" onchange={()=>{todo.done = !todo.done}} > {todo.text}
	{/if}
{/each}