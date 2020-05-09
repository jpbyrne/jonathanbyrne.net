<script>
	import Icon from './components/Icon.svelte';
</script>

<style>
	main {
		max-width: 640px;
	}

	h1 {
		background: linear-gradient(to bottom right, #3BB2B8 0%, #42E695 100%);
		-webkit-background-clip: text;
				background-clip: text;
		-webkit-text-fill-color: transparent;
		color: #3BB2B8;
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
</style>

<main>
    <h1>Hello.</h1>

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
