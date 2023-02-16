<template>
<li class="nav-element">
  <div v-html="icon"></div>
  <p>{{text}}</p>
</li>
</template>

<script>

export default {
  name: "SidebarLI",
  props: {
    icon: String,
    text: String
  },
}
</script>

<style lang="scss">
li.nav-element{
  opacity: 0.8;
  display: flex;
  align-items: center;
  list-style: none;
  font-size: 1rem;
  gap: 15px;
  padding: 5px 20px;
  margin: 10px auto;
  border-radius: 17px;
  svg{
    display: block;
    width: 2rem;
    height: 2rem;
    fill: white;
  }
  &:hover{
    background-color: white;
    color: black;
    cursor: pointer;
    svg{
      fill: black;
    }
  }
}
</style>