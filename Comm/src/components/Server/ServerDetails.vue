<template>
    <div class="col-xs-12 col-sm-6">
        <p v-if="!selectedServ">Server Details are currently not updated</p>
		<p v-else>Current status: {{selectedServ.status}}</p>
		<button @click="resetServer(selectedServ)">Reset</button>
    </div>

</template>

<script>

	export default {
		props: ['selectedServ'],
		methods: {
			resetServer(server){
				server.status = "Normal"
			}
		}
	}

</script>

<style>

</style>
