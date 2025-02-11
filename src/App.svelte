<script>
	import Icon from './components/Icon.svelte';
	import Header from './components/GradientHeader.svelte';

	// https://webgradients.com/
	const gradients = [
    {
			name: '012 Tempting Azure',
			left: '#84FAB0', right: '#8FD3F4'
		},
		{
			name: '019 Malibu Beach',
			left: '#4FACFE', right: '#00F2FE'
		},
		{
			name: '021 True Sunset',
			left: '#FA709A', right: '#FEE140'
		},
    {
			name: '112 Child Care',
			left: '#E8198B', right: '#C7EAFD'
		},
	];
	
	const gradient = gradients[Math.floor(Math.random() * gradients.length)];

	const favicon = document.querySelector('link[rel="icon"]');
	favicon.setAttribute('href', `favicons/${gradient.name}.png`);
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

    <p>I’m a Senior Software Developer at Workday Dublin.</p>
    <p>Previously I've worked at IBM, Accenture, Fjord, and IADT.</p>
    <p>Say <a href="mailto:hello@jonathanbyrne.net">hello@jonathanbyrne.net</a></p>

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
