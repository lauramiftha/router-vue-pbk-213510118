<template>
    <h1>Jobs</h1>
    <div v-for="job in jobs" :key="job.id" class="job">
        <router-link :to="{ name: 'JobDetails', params: { id: job.id }}">
            <h2>{{ job.title }}</h2>
        </router-link>
    </div>
    <div class="jobs">
    <div class="job">
      <h2>Front-end Developer</h2>
      <p>We are looking for a skilled front-end developer to join our team. In this role, you will be responsible for creating and maintaining the user interfaces for our web applications. The ideal candidate will have experience with HTML, CSS, and JavaScript, as well as a strong understanding of user experience design.</p>
      <h3>Qualifications</h3>
      <ul>
        <li>Proficient in HTML, CSS, and JavaScript</li>
        <li>Experience with front-end frameworks such as React or Vue</li>
        <li>Strong understanding of user experience design</li>
      </ul>
      <a href="#">Apply Now</a>
    </div>
    <div class="job">
      <h2>Back-end Developer</h2>
      <p>We are seeking a talented back-end developer to help build and maintain the server-side components of our web applications. The ideal candidate will have experience with server-side programming languages such as PHP, Python, or Ruby, as well as a solid understanding of databases and APIs.</p>
      <h3>Qualifications</h3>
      <ul>
        <li>Proficient in server-side programming languages such as PHP, Python, or Ruby</li>
        <li>Experience with databases and APIs</li>
        <li>Ability to work in a team environment</li>
      </ul>
      <a href="#">Apply Now</a>
    </div>
  </div>
</template>

<script>
export default {
    data() {
        return {
            jobs: [
                { title: 'Ninja UX Designer', id: 1, details: 'lorem'},
                { title: 'Ninja Web Developer', id: 2, details: 'lorem'},
                { title: 'Ninja Vue Developer', id: 3, details: 'lorem'},
            ]
        }
    }
}
</script>

<style>
.job h2{
    background: #f4f4f4;
    padding: 20px;
    border-radius: 10px;
    margin: 10px auto;
    max-width: 600px;
    cursor: pointer;
    color: #444;
}
.job h2:hover {
    background: #ddd;
}
.job a{
    text-decoration: none;
}
.jobs {
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
  }
  h1 {
    font-size: 36px;
    text-align: center;
    color: #333;
    margin-bottom: 20px;
  }
  .job {
    border: 1px solid #ccc;
    padding: 20px;
    margin-bottom: 20px;
  }
  h2 {
    font-size: 24px;
    margin-top: 0;
  }
  h3 {
    font-size: 18px;
    margin-top: 20px;
  }
  ul {
    margin: 0;
    padding: 0;
    list-style: none;
  }
  li {
    margin-bottom: 5px;
  }
</style>

