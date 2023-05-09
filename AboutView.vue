<template>
  <div class="about">
    <h1 class="title">Tentang Kami</h1>
    <div class="team-members">
      <div class="member">
        <img src="member1.jpg" alt="Anggota Tim 1">
        <h2>John Doe</h2>
        <p>Web Developer</p>
      </div>
      <div class="member">
        <img src="member2.jpg" alt="Anggota Tim 2">
        <h2>Jane Doe</h2>
        <p>UI/UX Designer</p>
      </div>
      <div class="member">
        <img src="member3.jpg" alt="Anggota Tim 3">
        <h2>Bob Smith</h2>
        <p>Mobile Developer</p>
      </div>
    </div>
    <p class="description">
      Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam aliquet tortor in sem feugiat, at euismod ante eleifend. Aenean feugiat lacus sed sagittis lacinia. Mauris ut ex euismod, imperdiet augue vel, finibus sapien. In suscipit, leo in bibendum hendrerit, orci mi imperdiet ipsum, nec rutrum velit ante a erat. Sed fermentum mauris sed quam sagittis tristique. Sed ac nisi eu tellus ullamcorper facilisis. Aliquam pellentesque tellus id fringilla tempor. Suspendisse sit amet ipsum ut massa lacinia sagittis. Morbi at turpis nisi. Duis vehicula velit nec volutpat vulputate. Praesent gravida nisl vel nunc dignissim ullamcorper. Curabitur tincidunt nulla velit, sit amet venenatis ipsum malesuada a.
    </p>
  </div>
</template>

<script>
export default {
  name: 'AboutView',
  components: { }
}
</script>

<style>
 .title {
    font-size: 36px;
    text-align: center;
    color: #333;
  }
  .team-members {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-top: 50px;
  }
  .member {
    flex: 1;
    text-align: center;
    margin: 0 10px;
  }
  .member img {
    width: 200px;
    height: 200px;
    object-fit: cover;
    border-radius: 50%;
    margin-bottom: 20px;
  }
  .member h2 {
    font-size: 24px;
    margin-bottom: 10px;
  }
  .member p {
    font-size: 18px;
    color: #666;
    margin-bottom: 20px;
  }
  .description {
    font-size: 18px;
    line-height: 1.5;
    color: #666;
    margin-top: 50px;
  }
</style>

