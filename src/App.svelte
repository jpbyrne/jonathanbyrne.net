<script>
	import Icon from './components/Icon.svelte';
	import Header from './components/GradientHeader.svelte';

	// https://webgradients.com/
	const gradients = [
    { left: '#3BB2B8', right: '#42E695' },
    { left: '#E8198B', right: '#C7EAFD' },
    { left: '#4fACFE', right: '#00F2FE' },
    { left: '#FA709A', right: '#FEE140' },
	];
	
	const gradient = gradients[Math.floor(Math.random() * gradients.length)];
</script>

<style>
	main {
		max-width: 640px;
	}

	h2 {
		margin: 21px 0;
	}

	p {
		margin-bottom: 12px;
	}

	p:last-child {
		margin-bottom: 0;
	}

	ul {
		display: flex;
		flex-direction: row;
		padding: 0;
		list-style: none;
	}

	a {
    color: var(--accent-color);
	}

	::selection {
			background: var(--accent-color);
			color: #FFFFFF;
	}
</style>

<main style="--accent-color: {gradient.left};">
    <Header gradient={gradient}>Hello.</Header>

    <h2>My name is Jonathan Byrne.</h2>

    <p>I’m a Frontend Developer at IBM Watson Health, based in Dublin.</p>
    <p>Previously I worked at Accenture The Dock, Fjord, and IADT.</p>
    <p>You can get in touch with me at <a href="mailto:hello@jonathanbyrne.net">hello@jonathanbyrne.net</a>.</p>

	<!-- <ul>
		<li>
			<a href="https://www.linkedin.com/in/jonathanpbyrne" target="_blank">
				<Icon symbol="linkedin" />
			</a>
		</li>
		<li>
			<a href="https://github.com/jpbyrne" target="_blank">
				<Icon symbol="github" />
			</a>
		</li>
		<li>
			<a href="https://twitter.com/_jpbyrne" target="_blank">
				<Icon symbol="twitter" />
			</a>
		</li>
	</ul> -->
</main>
