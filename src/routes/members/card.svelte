<script>
  /**
   * @type {{name: string; title: string; linkedin: string; email: string; imageUrl: string;}}
   
  */
  export let member;
</script>

<div class="card">
  <img class="member-image" src={member.imageUrl} alt={member.name} />

  <div class="card-content">
    <h3>{member.name}</h3>
    <p>{member.title}</p>
  </div>

  <div class="card-logo">
      {#if member.linkedin}
      <a href={member.linkedin} target="_blank" rel="noopener noreferrer">
          <img class="logo-linkedin" src="linkedin-logo.svg" alt="LinkedIn" />
        </a>
      {/if}
    {#if member.email}
    <a href={`mailto:${member.email}`}>
      <img class="logo-email" src="email-logo.svg" alt="Email" />
    </a>
    {/if}
    
  </div>
</div>
<style>
  .card {
    max-width: 400px;
    margin: 20px;
    border: 1px solid #ccc;
    border-radius: 2px;
    overflow: hidden;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    padding: 10px;
  }

  .member-image {
    width: 100%;
    height: 200px; 
    object-fit: cover;
  }

  .card-content {
    padding: 4px;
  }

  .card-logo {
    display: flex;
    justify-content: flex-end;
    align-items: flex-end;
    position: relative;
  }

  .logo-linkedin, .logo-email {
    width: 24px; 
    height: 24px; 
    padding: 2px;
    border-radius: 0%;
  }
  
</style>
