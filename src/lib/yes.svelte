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
	<div class="absolute left-5 top-5 flex">
		<LoveEmoji left={10} top={50}/>
		<LoveEmoji left={screenWidth-50} top={50}/>
	</div>
	<div class="absolute right-5 top-5 flex">
		<LoveEmoji left={10} top={50}/>
		<LoveEmoji left={screenWidth-50} top={50}/>
	</div>
</main>