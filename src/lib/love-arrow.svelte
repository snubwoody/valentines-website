<script lang='ts'>
    import { browser } from '$app/environment';
	import anime from 'animejs';
    import { onMount } from 'svelte';
	export let x = 0;
	export let y = 0;
	let loveArrow:HTMLElement;

	onMount(() => {
		let arrow = document.getElementById('love-arrow')
		animateArrow(arrow)
	})

	const animateArrow = (arrow:HTMLElement | null) => {
		anime({
			targets:loveArrow,
			scale:[0.0,1],
			duration:500,
			delay:1000,
			easing: 'easeInOutQuad'
		})
	}
</script>

<img 
src="/love-arrow.png" 
alt="" 
id="love-arrow"
bind:this={loveArrow}
style={`left: ${x}px; top: ${y}px`}
class={`w-[70px] aspect-square absolute`}>