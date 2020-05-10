<script>
  export let gradient;
</script>

<style>
	@keyframes flow {
		0% {
			background-position-x: 0;
		}
		50% {
			background-position-x: 100%;
		}
		100% {
			background-position-x: 0;
		}
  }

	h1 {
		animation: flow 7s ease-in-out infinite;
		background: linear-gradient(to right, var(--left-color), var(--right-color));
		background-size: 200%;
		-webkit-background-clip: text;
		background-clip: text;
		-webkit-text-fill-color: transparent;
		color: var(--gradient-left-color-1);
	}
</style>

<h1 style="--left-color: {gradient.left};--right-color: {gradient.right};">
  <slot />
</h1>
