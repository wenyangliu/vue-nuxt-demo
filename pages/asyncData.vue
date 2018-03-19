<template>
    <div>
        <h1>姓名：{{info.name}}</h1>
        <h2>年龄：{{info.age}}</h2>
        <h2>兴趣：{{info.interest}}</h2>
    </div>
</template>

<script>
    import axios from 'axios'
    export default {
      data() {
        return {
          name: 'hello'
        }
      },
      asyncData() {
        return axios.get('https://api.myjson.com/bins/prx5v')
          .then(res => {
            return {info: res.data}
          })
      }
    }
</script>