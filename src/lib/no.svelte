<script lang="ts">
    import anime from "animejs";
    import { onDestroy, onMount } from "svelte";
	let noDiv:HTMLElement;
	

	onMount(()=>{
		anime({
			targets: noDiv,
			scale:[0,1],
			bottom:['0px','100px'],
			duration:1100,
		})
	})

	
</script>

<div bind:this={noDiv} id="no-div" class="absolute bottom-5 flex flex-col items-center justify-center ">
	<!--
		<img src="/broken-heart.png" alt="" srcset="" class='w-[100px] aspect-square'>
	-->
	<div class='bg-[#FF4D6D] p-3 shadow-md rounded-md'>
		<p>Wrong answer try again</p>
	</div>
</div>