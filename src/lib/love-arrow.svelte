<script lang='ts'>
    import { browser } from '$app/environment';
	import anime from 'animejs';
    import { onMount } from 'svelte';
	export let x = 0;
	export let y = 0;
	let loveArrow:HTMLElement;

	onMount(() => {
		animateArrow()
	})

	const animateArrow = () => {
		anime({
			targets:loveArrow,
			scale:[0,1],
			duration:200,
			delay:500,
			easing: 'spring(1, 50, 5, 15)'
		})
	}
</script>

<img 
src="/love-arrow.png" 
alt="" 
bind:this={loveArrow}
style={`left: ${x}px; top: ${y}px`}
class={`w-[70px] aspect-square absolute`}>