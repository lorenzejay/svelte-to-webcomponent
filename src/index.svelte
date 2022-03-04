<svelte:options tag="my-counter" />

<script lang="ts">
	let status = 'start';
	let count = 0;

	function startTimer(){
		setInterval(() => {
		status = 'stop';
		count = count+1;
		},1000)
	}

	function dec() {
		count--;
	}
</script>

<style>
	* {
		font-size: 200%;
	}

	.input-btn {
		display: flex;
	}
</style>

<div>

	<div class="input-btn">
		<input />
		<button on:click={startTimer}>{status}</button>
	</div>
	<div>{count}</div>
</div>