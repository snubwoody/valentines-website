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
	<div class="absolute top-[9dvh] right-[15vw] rotate-12 w-fit h-fit shadow-lg bg-white border-b-[30px] border-[10px] border-white">
		<img src='/pic-1.webp' alt="" class='w-[30vw]'>
	</div>
	<div class="absolute top-[3dvh] left-[15vw] w-fit h-fit shadow-lg bg-white border-b-[30px] border-[10px] border-white">
		<img src='/pic-3.webp' alt="" class='w-[25vw] '>
	</div>
	<div class="absolute bottom-[1dvh] w-fit h-fit shadow-lg bg-white border-b-[30px] border-[10px] border-white">
		<img src='/pic-2.webp' alt="" class='w-[50vw] max-h-[40dvh] '>
	</div>
</main>