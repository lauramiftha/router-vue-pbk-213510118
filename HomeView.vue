<template>
  <h1>Selamat Datang Diberanda</h1>
    <nav>
    <form action="#" method="get">
      <input type="text" name="search" placeholder="Cari...">
      <button type="submit">Cari</button>
    </form>
  </nav>
  <!-- Konten -->
  <section>
    <article>
      <h2>Judul Artikel Pertama</h2>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Donec fringilla pharetra libero, id sagittis nisi imperdiet a. Sed sit amet turpis mi.</p>
    </article>
    <article>
      <h2>Judul Artikel Kedua</h2>
      <p>Proin a lorem eu dui pellentesque gravida nec ac ipsum. Nulla facilisi. Sed a commodo eros.</p>
    </article>

    <article>
      <h2>Judul Artikel Ketiga</h2>
      <p>Ut eu justo eget lacus molestie rutrum. Vivamus in libero arcu. In in faucibus felis, a semper sapien.</p>
    </article>
  </section>

  <!-- Footer -->
  <footer>
    <p>Hak Cipta © 2023</p></footer>
</template>

<script>
export default {
  name: 'HomeView',
  components: { }
}
</script>

<style>
nav {
      background-color: #444;
      color: white;
      display: flex;
      justify-content: space-between;
      padding: 10px;
    }

    /* CSS untuk konten */
    section {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      margin: 20px;
    }

    article {
      background-color: #eee;
      border: 1px solid #ccc;
      margin: 10px;
      padding: 10px;
      width: 300px;
    }
    article h2 {
      font-size: 24px;
      margin-top: 0;
    }

    article p {
      font-size: 14px;
      line-height: 1.5;
    }

    /* CSS untuk footer */
    footer {
      background-color: #333;
      color: white;
      padding: 10px;
      text-align: center;
    }
</style>
