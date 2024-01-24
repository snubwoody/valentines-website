<script lang='ts'>
    import LoveEmoji from "./love-emoji.svelte";
	import { browser } from "$app/environment";

	let screenWidth:number;
	let screenHeight:number;

	if(browser){
		screenWidth = window.screen.width;
		screenHeight = window.screen.height;
	}
	
</script>

<main class="w-screen h-screen fixed bg-white z-50 flex items-center justify-center">
	<p>She said yes</p>
	
	<div class="absolute left-2 top-0 flex flex-col justify-between h-screen">
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
	</div>
	<div class="absolute right-2 top-0 flex flex-col justify-between h-screen">
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
		<LoveEmoji/>
	</div>
</main>