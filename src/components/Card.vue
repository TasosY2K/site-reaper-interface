<template>
  <div class="card">
    <p>Ip Address: {{ info.ip }}</p>
    <p>Port: {{ info.port }}</p>
    <p>Title: {{ info.title }}</p>
    <a class="link" target="_blank" :href="'http://' + info.ip +':' + info.port">{{ 'http://' + info.ip + ':' + info.port }}</a>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    info: Object
  }
}
</script>

<style scoped>
.card {
  padding: 1rem;
  text-align: left;
  color: #e9e9e9;
  background-color: #292929;
  border-radius: 8px;
  transition-duration: 0.3s;
}

.card:hover {
  transform: translateY(-2px);
  -webkit-box-shadow: 0px 10px 27px -2px rgba(0,0,0,0.75);
  -moz-box-shadow: 0px 10px 27px -2px rgba(0,0,0,0.75);
  box-shadow: 0px 10px 27px -2px rgba(0,0,0,0.75);
}

.link {
  text-decoration: none;
  color: #FF2950;
  padding: 2px;
  border-radius: 8px;
  transition-duration: 0.3s;
}

.link:hover {
  color: #eeeeee;
  background-color: #FF2950;
}
</style>
