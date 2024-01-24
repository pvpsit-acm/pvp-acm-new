<script>
  import Card from "./card.svelte";
    const StuMembers = [
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      }
    ];
    const FacMembers = [
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "https://www.linkedin.com/in/johndoe/",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      },
      {
        name: "John Doe",
        title: "Software Engineer",
        linkedin: "",
        email: "john.doe@example.com",
        imageUrl: "teja-2.jpg",
      }
    ];
</script>
<div>
    <h2>Studnet Members</h2>
</div>
<div class="members">
{#each StuMembers as member (member.name)}

    <Card {member} />
 
{/each}
 </div>
 <div>
    <h2>Faculty Members</h2>
</div>
<div class="members">
{#each FacMembers as member (member.name)}
<Card {member} />
{/each}
 </div>
<style>
    .members {
      display: flex;
      flex-direction: row;
      flex-wrap: wrap;
      justify-content: space-between;
      grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
      padding-left: 10%;
      padding-right: 10%;
      justify-content: space-between;
		justify-content:flex-start;
		align-items: flex-start;
    }
    @media (max-width: 768px) {
      .members {
        flex-direction: column;
        align-items: center;
      }
    }
</style>
