<template>
  	<div class="hello">
    	<h1>{{ msg }}</h1>
		<p>Message: {{ message }}</p>
    	<div><input v-model="message" placeholder="edit me"></div>
	</div>
</template>

<script>
export default {
	name: 'Chat',
    props: {
        msg: String
    },
    data: function() {
        return {
            message: 'test'
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
