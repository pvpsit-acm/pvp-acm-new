<!-- Quote.svelte -->
<script>
    export let quote;
    export let author;
  </script>
  
  <style>
    .quote-container {
      display: flex;
      justify-content: center;
      align-items: center;
      text-align: center;
      margin: 20px;
    }
  
    .quote-text {
      font-style: italic;
      padding: 10px;
      border-left: 5px solid #3498db; /* Highlight color on the left side */
      border-right: 5px solid #3498db; /* Highlight color on the right side */
    }
  </style>
  
  <div class="quote-container">
    <blockquote class="quote-text">
      <p>{quote}</p>
      {#if author}
        <footer>- {author}</footer>
      {/if}
    </blockquote>
  </div>
  