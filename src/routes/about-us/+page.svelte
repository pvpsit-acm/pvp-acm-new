<script>
    import Image from '../../lib/components/image.svelte';
    const images =[ {src:'AboutUs/acm_desktopcta.jpeg',title:'AboutPage'}]
</script>
<div class="container ">
    <div class="side-by-side">
        <p>
            Association for Computing Machinery (ACM), the world’s largest educational and scientific computing society established in 1947, delivers resources that advance computing as a science and a profession. It is a not-for-profit professional membership group. Its headquarters are in New York City.ACM provides the computing field’s premier Digital Library and serves its members (100000+ worldwide) and the computing profession with leading-edge publications, conferences, and career resources.
                <br><br>
            The A.M. Turing Award, widely regarded as “the Noble Prize in computing” and the ACM’s most prestigious technical award, is given for major contributions of lasting importance to computing. Recipients are invited to give the annual A.M. Turing Award Lecture. The award is also accompanied by as cash prize of $1,000,000, which in recent years has been underwritten by the Intel Corporation and Google Inc.
                <br><br>
            Under Department of CSE, PVP Siddhartha Inst. of Tech Vijayawada ACM Student Chapter, since its inception in 2011 has been continuously engaged in conducting and organizing various activities like Guest lectures,workshops,coding contests etc., for the benefit of students. The strength of chapter is the students itself who are themselves office bearers,organizers,event handlers.ACM student chapter in its true sense maintained by students.ACM chapter website is too maintained by student web master. Students are assisted by faculty co-ordinators and ACM Student chapter Sponsor (In-charge).
        </p>
    </div>
    <div class="side-by-side">
        <img src={images[0].src} title={images[0].src}>
    </div>
<style>
    div{
        text-align: justify
    }
    .container {
    display: flex;
  }

  .side-by-side {
    flex: 1;
    margin: 10px;
    padding: 20px;
    /* border: 1px solid #ccc; */
    font-weight:bold
  }
  
</style>
</div>