<script>
  import { onMount } from "svelte";

  export let src = String();
  export let title = String();
  let isOpen = false;

  function openImage() {
    isOpen = true;
  }

  function closeImage() {
    isOpen = false;
  }

  onMount(() => {
    document.addEventListener("keydown", handleKeyPress);
    return () => {
      document.removeEventListener("keydown", handleKeyPress);
    };
  });

  function handleKeyPress(event) {
    if (event.key === "Escape") {
      closeImage();
    }
  }
</script>

{#if isOpen}
  <!-- svelte-ignore a11y-click-events-have-key-events -->
  <div class="overlay" on:click={closeImage}>
    <div class="modal">
      <span class="close-button" on:click={closeImage}>&times;</span>
      <img src={src} alt={title} />
      <div class="image-title">{title}</div>
    </div>
  </div>
{/if}

<div class="image-frame" on:click={openImage}>
  <img src={src} alt={title} />
</div>

<style>
  /* Existing styles remain unchanged */
  .image-frame {
    border: 2px solid #ddd; /* Border color for the frame */
    padding: 10px;
    text-align: center;
    margin: 10px;
    border-radius: 5px;
    max-width: fit-content;
    margin-left:2em;
  }

  img {
    max-width: 100%;
    max-height: 450px; /* Adjust the maximum height as needed */
    border-radius: 5px; /* Optional: Add border-radius to the image */
  }

  .image-title {
    margin-top: 10px;
    font-size: 14px;
    color: #333;
  }
  .overlay {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.7);
    display: flex;
    justify-content: center;
    align-items: center;
    z-index: 1;
  }

  .modal {
    max-width: 80%;
    max-height: 80%;
    overflow: hidden;
    position: relative;
    animation: fadeIn 0.3s ease;
  }

  .modal img {
    width: 100%; /* Make the image fill the modal */
    height: 100%; /* Make the image fill the modal */
  }

  .close-button {
    position: absolute;
    top: 10px;
    right: 10px;
    font-size: 20px;
    color: #fff;
    cursor: pointer;
  }

  @keyframes fadeIn {
    from {
      opacity: 0;
      transform: scale(0.8);
    }
    to {
      opacity: 1;
      transform: scale(1);
    }
  }
</style>
