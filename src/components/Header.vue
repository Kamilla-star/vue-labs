<template>
  <header>
    <a class="logo" href="/">Камилла Саттарова</a>
    <nav>
      <p><router-link to="/">Главная</router-link></p>
      <p><router-link to="/news">Новости</router-link></p>
    </nav>
  </header>
</template>

<script>
export default {
  name: "Header",
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #ff87ab;
  color: #fff;
  padding: 7px 20px;
}

nav {
  display: flex;
}

p {
  margin-right: 25px;
}

p:last-child {
  margin-right: 0;
}

a {
  text-decoration: none;
  color: #fff;
}
a:hover {
  text-decoration: underline;
}

</style>