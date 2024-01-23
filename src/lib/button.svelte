<script lang='ts'>
	//export let fn: () => void | VoidFunction;
</script>

<button
on:click={($event) => {}} 
id='btn' 
class='w-44 h-10 rounded justify-center items-center flex gap-2 bg-red-300'
>
	<slot/>
</button>