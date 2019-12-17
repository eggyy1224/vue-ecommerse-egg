<template>
  <div>
    <a href="#" @click.prevent="signout">登出</a>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      
    }
  },
  methods: {
    signout() {
      const vm = this;
      const api = `${process.env.APIPATH}/logout`;

      this.$http.post(api).then((response) => {
        if (response.data.success) {
          vm.$router.push('/login');
        }
      }); 
    }
  }
}
</script>