<template>
    <div>
        <h2>News-Content [{{ $route.params.id }}]</h2>
        <ul>
            <li><a href="/">Home</a></li>
        </ul>
    </div>
</template>

<script>
    export default {
      validate({params}) {
        return /^\d+$/.test(params.id)
      },
      data(){
        return {
          title: this.$route.params.title
        }
      },
      head() {
        return {
          title: this.title,
          meta: [
            {hid: 'description', name: 'news', content: 'This is news page'}
          ]
        }
      }
    }
</script>