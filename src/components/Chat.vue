<template>
	<v-container fluid grid-list-md>
		<v-flex xs6 offset-xs3>
			<v-card-text>
				<v-list ref="chat" id="logs">
				    <template v-for="(mess, index) in messages">
					    <div class="text">
						    <v-subheader v-if="mess" :key="index">{{ mess }}</v-subheader>
						</div>
				  </template>
				</v-list>
			</v-card-text>
		</v-flex>
		<v-layout align-end justify-center row fill-height/>
	        <v-flex xs6 offset-xs3>
	          <v-textarea
	            solo
	            name="input"
	            label="Solo textarea"
	            v-model="message"
	          ></v-textarea>
	        </v-flex>
			<v-flex xs4 offset-xs8>
				<div>
					<v-btn color="success" @click="addMessage()">Отправить</v-btn>
				</div>
			</v-flex>
	    </v-layout>
    </v-container>
</template>

<script>
  	export default {
	    data: () => ({
			message: '',
			messages: [],
	    }),
		methods: {
		    addMessage() {
		      	this.messages.push(this.message);
				this.message = "";
		  	}
		},
		watch: {
		    messages() {
			    setTimeout(() => {
			        this.$refs.chat.$el.scrollTop = this.$refs.chat.$el.scrollHeight;
			    }, 1000);
		    }
		}
  	}
</script>

<style>
#logs {
  	height: 60vh;
  	overflow: auto;
  	position: relative;
}
.text {
	position: relative;
	bottom: 0;
	margin-bottom: 10px;
}
</style>
