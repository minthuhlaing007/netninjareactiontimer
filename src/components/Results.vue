<template>
	<p>Reaction Time --  {{ score }}</p>
	<p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  name: 'Results',
  props:["score"],
  data () {
    return {
    	rank:null,
    }
  },
  mounted(){
  	if(this.score < 250){
  		this.rank = "Ninja Fingers"
  	}else if(this.score < 400){
  		this.rank = "Rapid Reflexes"
  	}else{
  		this.rank = "Snail pace..."
  	}
  }
}
</script>

<style lang="css" scoped>
.rank{
	font-size: 1.4em;
	color: #0faf87;
	font-weight: bold;
}
</style>