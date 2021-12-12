<script>
	let subjects = [
		'gerecht',
		'zanger',
		'liedje',
		'gebouw',
		'plek',
		'BN\'er',
		'beroep',
		'dier',
		'zoogdier',
		'insect',
		'kledingstuk',
		'kledingmerk',
		'vissoort',
		'vogelsoort',
		'plant',
		'ster of planeet',
		'pizzaingredient',
		'schoolvak'
	];
	const alphabet = ["A","B","C","D","E","F","G","H","I","J","K","L","M","N","O","P","Q","R","S","T","U","V","W","X","Y","Z"];
	let letter = alphabet[Math.floor(Math.random() * alphabet.length)];
	let subject = subjects[Math.floor(Math.random() * subjects.length)];

	function random() {
		letter = alphabet[Math.floor(Math.random() * alphabet.length)];
		subject = subjects[Math.floor(Math.random() * subjects.length)];
	}
</script>

<div class="card" on:click={random}>
	<p>Noem een</p>
	<p class="subject">{subject}</p>
	<p>met de letter</p>
	<p class="letter">{letter.toUpperCase()}</p>
	<p><small>klik voor het volgende kaartje</small></p>
</div>

<style>
	:global(body) {
		padding: 1rem;
	}
	* {
		font-size: 1.5rem;
	}
	.card {
		padding: 1rem;
		margin: .5rem;
		border: 1px solid #808080;
		box-shadow: 2px 5px 5px 5px #b4b4b4;
		border-radius: 10px;
		background-color: #f0f0f0;
		max-width: 700px;
		text-align: center;
	}
	.card:active {
		box-shadow: inset 3px 3px 3px #b4b4b4;
	}
	p {
		margin: 10px;
	}
	.subject, .letter {
		font-size: 3rem;
		font-weight: 700;
	}
	.subject {
		font-style: italic;
	}
	small {
		font-size: 70%;
		font-style: italic;
	}
</style>
