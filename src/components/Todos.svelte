<script>
	import { ButtonGroup, Button } from 'flowbite-svelte';

	let todos = []	
	let task = ""
	let startTime = ""
	let endTime = ""

    const addNewTodo = async () => {
    }

    // @ts-ignore
    const markTodoComplete = async (item) => {
    }
    
    const deleteTodo = async (item) => {
    }
    
    const altAddTodo = (event) => {
    }
</script>

<div class="todo-wrapper">

	<h2>Add Todo</h2>

	<label class="label">
		<input type="text" placeholder="Add Task" bind:value={task} class="input"/>
	</label>
	<label class="label">
		<input type="text" placeholder="Start Time" bind:value={startTime} class="input"/>
	</label>
	<label class="label">
		<input type="text" placeholder="End Time" bind:value={endTime} class="input"/>
	</label>
	<button on:click={addNewTodo} class="">
	Add Todo
	</button>

	<ol>
		{#each todos as item}
			<li class:complete={item.isComplete}>
				{item.task}
				<span>
					<button on:click={() => markTodoComplete(item)} class="">*</button>
					<button on:click={() => deleteTodo(item)}>x</button>
				</span>
			</li> 
		{:else}
			<p>No todos found</p>
		{/each}
	</ol>
</div>

<style>
	.todo-wrapper{
		display: flex;
		background: #fff;
		margin: 2rem 0 4rem 0;
		padding: 1rem;
		position: relative;
		box-shadow: 0 2px 4px 0 rgba(0, 0, 0, 0.2), 0 2.5rem 5rem 0 rgba(0, 0, 0, 0.1);flex-direction: column;
	}
	
	.label {
		line-height: 1.01567;
		font-weight: 300;
		padding: 0.8rem;
		margin-bottom: 1rem;
		text-align: center;
		padding: 2rem;
		border: 2px solid #000;
	}
	
</style>