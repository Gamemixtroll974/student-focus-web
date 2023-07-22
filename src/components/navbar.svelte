<script lang="ts">
	import MdPerson from 'svelte-icons/md/MdPerson.svelte';
	import { circInOut } from 'svelte/easing';
	import { fade } from 'svelte/transition';
	import '../styles/+page.scss';
	let toggleProfile = false;
</script>

<nav class="nav">
	<div class="left-items">
		<div class="title">
			<h1>Student Focus</h1>
		</div>
	</div>
	<div class="center-items">
		<a href="/">Accueil</a>
		<a href="/notes">Notes</a>
		<a href="/pomodoro">Pomodoro</a>
		<a href="/concentration">Concentration</a>
	</div>
	<div class="right-items">
		<div class="icon" on:click={() => (toggleProfile = !toggleProfile)}>
			<MdPerson />
		</div>
		{#if toggleProfile}
			<div class="profile" transition:fade={{ delay: 100, duration: 500, easing: circInOut }}>
				<a href="/connexion">Connexion</a>
				<a href="/inscription">Inscription</a>
			</div>
		{/if}
	</div>
</nav>
