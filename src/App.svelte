<script lang="ts">
	let rightSound: HTMLAudioElement | null = null;
	let wrongSound: HTMLAudioElement | null = null;

	const playRightSound = () => {
		if (rightSound) return rightSound.play();
	};
	const playWrongSound = () => {
		if (wrongSound) return wrongSound.play();
	};</script>

<main>
  <audio bind:this={rightSound} src="right.mp3" preload="auto"></audio>
<audio bind:this={wrongSound} src="wrong.mp3" preload="auto"></audio>

  <div class="background flex h-svh flex-col items-center justify-center gap-10 bg-slate-800">
    <!-- Button to trigger the sound effect -->
  
    <button class="button thumbs-up" on:click={playRightSound} aria-label="A thumbs-up button"
    ></button>
    <button class="button thumbs-down" on:click={playWrongSound} aria-label="A thumbs-down button">
    </button>
  </div>
  
</main>
