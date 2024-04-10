<template>
  <nav>
    <a href="#">
      <img src="" alt="" />
      <p>Hyperhire</p>
    </a>
    <ul>
      <li>
        <a href="#">
          Home
          <q-icon name="fa-solid fa-chevron-down" />
        </a>
      </li>
      <li><a href="#">About</a></li>
    </ul>
    <button>Login</button>
  </nav>
</template>

<script setup>
defineOptions({
  name: "TopHeader",
});
</script>
<style lang="scss" scoped>
nav {
  background-color: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-direction: row;
  width: 80%;
  margin: auto;
  a {
    color: white;
  }
  ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
    overflow: hidden;
    li {
      float: left;
      a {
        display: block;
        color: white;
        text-align: center;
        padding: 14px 16px;
        text-decoration: none;
        &:hover {
          background-color: #111;
        }
      }
    }
  }
}
</style>
