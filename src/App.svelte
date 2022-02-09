<script>
	import Age from './components/Age.svelte'
	let name = 'Amy'
	let age = 35
	$: dogAge = age * 7 // React variable, reacts to 'age' changes

	const add = () => age++
	const minus = () => age--
</script>

<style>
	h1 {
		color: red
	}
</style>

<h1>
	Hello {name}
</h1>
<Age {age} />
<Age age={dogAge} yearType='dog'/>
<button on:click={add}>+</button>
<button on:click={minus}>-</button>