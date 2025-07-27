<script lang="ts">

  let rightSound: HTMLAudioElement | null = null
  let wrongSound: HTMLAudioElement | null = null
  let completeSound: HTMLAudioElement | null = null

  const playRightSound = () => {
    if (rightSound) return rightSound.play()
  }
  const playWrongSound = () => {
  const playCompleteSound = () => {
    completeSound?.play()
  }
</script>

<main>
  <audio bind:this={rightSound} src="right.mp3" preload="auto"></audio>
  <audio bind:this={wrongSound} src="wrong.mp3" preload="auto"></audio>
  <audio bind:this={completeSound} src="complete.mp3" preload="auto"></audio>

  <div
    class="background flex h-svh flex-col items-center justify-center gap-10 bg-slate-800"
  >
    <!-- Button to trigger the sound effect -->

    <button
      class="button right"
      on:click={playRightSound}
      aria-label="A right meerkat button"
    ></button>
    <button
      class="button wrong"
      on:click={playWrongSound}
      aria-label="A wrong meerkat button"
    >
    </button>
  <button
      class="button complete"
      on:click={playCompleteSound}
      aria-label="A complete sparkles button"
    >
    </button>
  </div>
</main>
