<script lang='ts'>
    import { browser } from '$app/environment';
	import anime from 'animejs';
    import { onMount } from 'svelte';
	export let left = 0;
	export let top = 0;
	export let bottom = 0;
	export let right = 0;
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
style={`
left: ${left}px; 
top: ${top}px;
bottom: ${bottom}px;
right: ${right}px;
`
}
class={`w-[70px] aspect-square absolute`}>