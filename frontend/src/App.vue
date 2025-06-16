<template>
  <div>
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'Loading...'
    }
  },
  mounted() {
    fetch('http://localhost:5000/api/hello')
      .then(res => res.json())
      .then(data => {
        this.message = data.message
      })
      .catch(() => {
        this.message = 'Failed to fetch from backend'
      })
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
