<script>
  export let src=String();
  export let title=String();
</script>

<div class="image-frame">
  <img src={src} alt={title} />
</div>

<style>
  .image-frame {
    border: 2px solid #ddd; /* Border color for the frame */
    padding: 10px;
    text-align: center;
    margin: 10px;
    border-radius: 5px;
    max-width: fit-content;
  }

  img {
    max-width: 100%;
    max-height: 250px; /* Adjust the maximum height as needed */
    border-radius: 5px; /* Optional: Add border-radius to the image */
  }

  .image-title {
    margin-top: 10px;
    font-size: 14px;
    color: #333;
  }
</style>
