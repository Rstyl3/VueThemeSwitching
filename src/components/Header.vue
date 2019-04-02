<template>
  <header>
    <nav id="navbar">
      <ul>
        <li>
          <a href="#">home</a>
        </li>
        <li>
          <a href="#">about</a>
        </li>
        <li>
          <a href="#">contact</a>
        </li>
      </ul>
    </nav>
  </header>
</template>

<script>
export default {

}
</script>

<style scoped>
#navbar {
    padding: 20px 0;
    font-size: 24px;
}
#navbar a {
  color: var(--primary);
}
#navbar > ul {
    display: flex;
    justify-content: space-evenly;
    margin: 0 auto;
    padding: 0;
    list-style-type: none;
}
</style>
