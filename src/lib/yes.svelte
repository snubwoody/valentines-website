<script lang='ts'>
    import LoveEmoji from "./love-emoji.svelte";
	import { browser } from "$app/environment";
    import PicFrame from "./pic-frame.svelte";

	let screenWidth:number;
	let screenHeight:number;

	if(browser){
		screenWidth = window.screen.width;
		screenHeight = window.screen.height;
	}
	
</script>

<main class="w-screen h-screen fixed bg-white z-50 flex items-center justify-center">
	<div class="flex">
		<LoveEmoji/>
		<p>She said yes</p>
		<LoveEmoji/>
	</div>
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
	<div class="absolute top-44 right-16 rotate-12">
		<PicFrame imgSrc='/pic-1.jpeg' width={120}/>
	</div>
	<div class="absolute top-5 left-20">
		<PicFrame imgSrc='/pic-3.jpeg' width={100}/>
	</div>
	<div class="absolute bottom-5">
		<PicFrame imgSrc='/pic-2.JPG' width={250}/>
	</div>
</main>