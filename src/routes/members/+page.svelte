<script>
  import Card from "./card.svelte";
    const StuMembers = [
      {
        name: "N Sampreeth Chowdary",
        title: "Chair",
        linkedin: "https://www.linkedin.com/in/sampreeth3217",
        email: "nschowdary1234@gmail.com",
        imageUrl: "student_members/chair.png",
      },
      {
        name: "Pavan Kumar Chennupati",
        title: "Vice Chair",
        linkedin: "https://www.linkedin.com/in/pavankch/",
        email: "pavankc005@gmail.com",
        imageUrl: "student_members/vicechair.png",
      },
      {
        name: "G Gowtham Chowdary",
        title: "Secretary",
        linkedin: "https://www.linkedin.com/in/gowtham-chowdary-garapati-21b24a2b9/",
        email: "garapatigowtham6@gmail.com",
        imageUrl: "student_members/secretary.png",
      },
      {
        name: "Siddhartha Yalamanchili",
        title: "Web Master",
        linkedin: "https://www.linkedin.com/in/siddhartha-yalamanchili",
        email: "sidduyalamanchili3@gmail.com",
        imageUrl: "student_members/webmaster.png",
      },
      {
        name: "Katta Jaya Siva Srithan",
        title: "Treasurer",
        linkedin: "https://www.linkedin.com/in/srithan-katta",
        email: "srithankatta9@gmail.com",
        imageUrl: "student_members/treasurer.png",
      },
      {
        name: "Sai Lalith Kistamsetti",
        title: "Membership Chair",
        linkedin: "https://www.linkedin.com/in/kistamsetti-sai-lalith-b49602263",
        email: "mrsailalith@gmail.com",
        imageUrl: "student_members/membershipchair.png",
      }
    ];
    const FacMembers = [
      {
        name: "Dr. M. V. Ramakrishna",
        title: "Faculty Sponsor",
        linkedin:"",
        email: "mvrk@pvpsiddhartha.ac.in",
        imageUrl: "faculty/faculty_sponsor.webp",
      },
      {
        name: "Dr. J. Rama Devi",
        title: "Faculty Coordinator",
        linkedin:"",
        email: "ramadevi@pvpsiddhartha.ac.in",
        imageUrl: "faculty/facultyco1.webp",
      },
      {
        name: "Ms. T. Sri Lakshmi",
        title: "Faculty Coordinator",
        linkedin:"",
        email: "tslakshmi@pvpsiddhartha.ac.in",
        imageUrl: "https://www.pvpsiddhartha.ac.in/images/CSESTAFF/CSE010063.jpg",
      }
    ];
</script>
<div>
    <h2>Student Members</h2>
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
