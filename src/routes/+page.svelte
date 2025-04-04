<script>
	import Card1 from '../components/Card1.svelte';
	import Card2 from '../components/Card2.svelte';4
	import Card3 from '../components/Card3.svelte';
	import Card4 from '../components/Card4.svelte';
	import Card5 from '../components/Card5.svelte';
	import Card6 from '../components/Card6.svelte';
	import Text from '../components/Text.svelte';
	import Card from './Card.svelte';
	import Header from '../components/Header.svelte';

	let formData = {
		name: '',
		bday: '',
		email: '',
		step: 0,
		error: ''
	};
	let step = 0;

	function onclick() {
		if (formData.name === '') {
			formData.error = 'Please enter your name';
		} else {
			formData.step += 1;
			formData.error = '';
		}
	}
	function bday() {
		if (formData.bday === '') {
			formData.error = 'Please enter your birthday';
		} else {
			formData.step += 1;
			formData.error = '';
		}
	}

	function back() {
		formData.step -= 1;
	}
	function step1() {
		formData.step += 1;
	}

	// function email() {
	// 	if (formData.email === '') {
	// 		formData.error = 'Please enter your email';
	// 	} else {
	// 		formData.step += 1;
	// 		formData.error = '';
	// 	}
	// }
</script>

<div class="main">
	<div class="bg-col"></div>
	{#if formData.step === 0}
		<!-- <div class="container">
			<h1
				class="head1"
				style="font-family: Funnel Display; font-weight: 500; font-size: 5rem; text-align: center; "
			>
				Welcome
			</h1>
			<h2
				style="font-family: Poppins; font-weight: 300; font-size: 23px; text-align: center; "
			>
				Your Ultimate Space
			</h2>
		</div> -->
	<Header />
		<div class="review">
		<span class="first">Review and Comment</span> <br> <span class="second">Check topics and trends</span> <br> <span class="third"> what people really like </span>
		</div>
		<Card3  />
		<Card4 />
		<Card5 />
		<Card2  />
		<Card1  />

		<Card6 />
		<Text />
		
		<button class="btn-1" onclick={step1}> Get Started <i class="ri-arrow-right-up-long-line"></i></button>
	{/if}
	{#if formData.step === 1}
		Step: {formData.step}

		<label for="name">Name</label><br />
		<input type="text" class="input" id="name" bind:value={formData.name} />

		{#if formData.error}
			<p style="color: red;">{formData.error}</p>
		{/if}

		<button {onclick}>Next</button>
	{/if}
	{#if formData.step === 2}
		Step: {formData.step}
		<label for="name">Name</label><br />
		<input placeholder="Email address" class="input" name="text" type="email" />
		<input placeholder="Password" class="input" name="password" type="password" />
		{#if formData.error}
			<p style="color: red;">{formData.error}</p>
		{/if}
		<button onclick={back}>Previous</button>
		<button {onclick}>Next</button>
	{/if}
	{#if formData.step === 3}
		Step: {formData.step}
		<label for="bday">Name</label><br />
		<input type="date" id="bday" bind:value={formData.bday} />

		{#if formData.error}
			<p style="color: red;">{formData.error}</p>
		{/if}
		<button onclick={back}>Previous</button>
		<button onclick={bday}>Next</button>
	{/if}
	<!-- </div> -->
</div>
{#if formData.step === 4}
	<Card />
{/if}

<style>
	.main {
		width: 100%;
		height: 100vh;
	}
	.bg-col {
		background: radial-gradient(
			125% 125% at -2% 101%,
			rgba(234, 105, 35, 0.754) 10.5%,
			rgba(255, 124, 1, 0.725) 16%,
			rgba(232, 138, 16, 0.775) 17.5%,
			rgba(245, 170, 100, 0.837) 25%,
			rgba(238, 174, 202, 1) 40%,
			rgba(202, 179, 214, 1) 65%,
			rgba(148, 201, 233, 1) 100%
		);
		width: 100%;
		height: 180%;
		position: absolute;
		top: 0;
		left: 0;
		z-index: -1;
	}
	.container {
		margin: 5rem;
		padding-left: 3rem;
		padding-right: 3rem;
		width: 86%;
		height: 15vh;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background-color: #f7f7f7;
		border: 1.5px solid #000;
		border-radius: 0.5rem;
		box-shadow: 2.5px 3px 0 #000;
	}
	.review{
		font-family: Poppins;
		font-weight: 500;
		position: absolute;
		
		top: 50%;
		left: 50%;
		text-align: center;
		transform: translate(-50%, -50%);
		line-height: 1;
		margin-top: 5rem;
	}
	.review .first{
		color: #fff;
		font-size: 3.5rem;
		letter-spacing: -0.3rem;
	}
	.review .second{
		color: #fff;
		font-size: 4rem;
		letter-spacing: -0.3rem;
	}
	.review .third{
		color: #fff;
		font-size: 5rem;
		letter-spacing: -0.3rem;
	}
	.input {
		max-width: 190px;
		padding: 0.875rem;
		font-size: 1rem;
		border: 1.5px solid #000;
		border-radius: 0.5rem;
		box-shadow: 2.5px 3px 0 #000;
		outline: none;
		transition: ease 0.25s;
	}

	.input:focus {
		box-shadow: 5.5px 7px 0 black;
	}
	button {
		font-family: Goblin One;
		background-color: white;
		color: black;
		border-radius: 0.6em;
		font-size: 25px;
		font-weight: 300;
		cursor: pointer;
		transition: all 0.3s ease-in-out;
		border: 1px solid black;
		box-shadow: 2px 5px 0 0 black;
		
	}

	button:hover {
		transform: translateY(-2px) translateX(-1px);
		box-shadow: 5.5px 7px 0 black;
	}
	button:focus {
		outline: none;
		box-shadow: 5.5px 7px 0 black;
	}
	button:active {
		transform: translateY(2px) translateX(1px);
		box-shadow: 0 0 0 0 black;
	}

	.btn-1 {
		display: flex;
		justify-content: center;
		align-items: center;
		font-size: 2rem;
		font-family: Goblin One;
		font-weight: 600;
		position: absolute;
		top: 87%;
		left: 52%;
		cursor: pointer;
		width: 400px;
		height: 70px;
	}
	.btn-1 i{
		width: 1.5rem;
		height: 1.5rem;
		font-size: 1.5rem;
		margin-left: 0.5rem;
	}

</style>
