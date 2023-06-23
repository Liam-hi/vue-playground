<template>
    <div>
        <h1>{{ text }}</h1>
    </div>
</template>

<script>
export default {
    props: {
      text: {
        type: String,
        default: "Default text"
      }
    }
  }
  </script>

<style scoped>

div {
    display: flex;
    align-items: center;
    justify-content: center;
    background: pink;
    height: 128px;
    width: 128px;
}
</style>