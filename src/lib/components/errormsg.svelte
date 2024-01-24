<script>
    let showErrorMessage = true;
  
    function closeErrorMessage() {
      showErrorMessage = false;
    }
  </script>
  
  {#if showErrorMessage}
    <div class="error-message">
      <p>
        In case the content is not displaying, please reload it.
        <!-- svelte-ignore a11y-click-events-have-key-events -->
        <span class="close-button" on:click={closeErrorMessage}>close</span>
      </p>
    </div>
  {/if}
  
  <style>
    .error-message {
      border: 2px solid #ece6e6; /* Red border for warning */
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); /* Box shadow for a subtle effect */
      padding: 5px;
      margin: 10px 0;
      border-radius: 5px;
      background-color: #fff; /* White background */
      width: 500px;
      position: relative;
      align-items: center;
      align-self: center;
    }
  
    .close-button {
      cursor: pointer;
      float: right;
      font-weight: bold;
      color: #333;
      border-radius: 5px solid #333;
      background-color: rgba(0, 0, 0, 0.1);
      padding: 0 5px;
    }
  </style>