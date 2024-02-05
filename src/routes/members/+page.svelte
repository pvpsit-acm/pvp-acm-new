<script>
  import Card from "./card.svelte";
    const StuMembers = [
      {
        name: "K Pavithra Sai",
        title: "Student Chair",
        linkedin: "https://www.linkedin.com/in/pavithra-sai-kadiyala/",
        email: "20501A0571@pvpsit.ac.in",
        imageUrl: "student_members/studentchair.jpg",
      },
      {
        name: "G.Venkata Raju",
        title: "Student Vice Chair",
        linkedin: "https://www.linkedin.com/in/venkataraju-gogudesi-7051a1252/",
        email: "20501A0553@pvpsit.ac.in",
        imageUrl: "student_members/studentvicechair.jpg",
      },
      {
        name: "N.Teja",
        title: "Treasurer",
        linkedin: "https://www.linkedin.com/in/narayana-teja/",
        email: "20501A05D3@pvpsit.ac.in",
        imageUrl: "student_members/treasurer.jpg",
      },
      {
        name: "Vamsi Saripudi",
        title: "Web Master",
        linkedin: "https://www.linkedin.com/in/vamsi-saripudi-a3051b1b6/",
        email: "20501A05H9@pvpsit.ac.in",
        imageUrl: "student_members/webmaster.jpg",
      },
      {
        name: "K.Yaswant Sai",
        title: "Secretary",
        linkedin: "https://www.linkedin.com/in/yaswant-sai-kavuri/",
        email: "20501A05J1@pvpsit.ac.in",
        imageUrl: "student_members/secretary.jpg",
      },
      {
        name: "Sahiti Lavu",
        title: "Membership Chair",
        linkedin: "https://www.linkedin.com/in/sahiti-lavu-7766a5214",
        email: "20501a0599@pvpsit.ac.in",
        imageUrl: "student_members/membershipchair.webp",
      },
      {
        name: "Dasari Hitesh",
        title: "Member",
        linkedin: "https://www.linkedin.com/in/dasari-hitesh-33162426a/",
        email: "20501a0566@pvpsit.ac.in",
        imageUrl: "student_members/member1.jpg",
      },
      {
        name: "VSN Himaja",
        title: "Member",
        linkedin: "https://www.linkedin.com/in/vemuri-sri-naga-himaja-b01a74215/",
        email: "20501a05I3@pvpsit.ac.in",
        imageUrl: "student_members/member2.jpg",
      },
      {
        name: "Pragna Y",
        title: "Member",
        linkedin: "https://www.linkedin.com/in/pragna-yanduri-781193245/",
        email: "21501A05J5@pvpsit.ac.in",
        imageUrl: "student_members/member3.jpg",
      },
      {
        name: "Somu Likitha",
        title: "Member",
        linkedin: "http://www.linkedin.com/in/somu-likitha-a1724a245",
        email: "21501A05G5@pvpsit.ac.in",
        imageUrl: "student_members/member4.jpg",
      },
      {
        name: "Sravya Kodali",
        title: "Member",
        linkedin: "https://www.linkedin.com/in/sravya-kodali-60626422b",
        email: "21501A0585@pvpsit.ac.in",
        imageUrl: "student_members/member5.jpg",
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
        imageUrl: "faculty/facultyco2.webp",
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
