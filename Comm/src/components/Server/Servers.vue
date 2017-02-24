<template>
    <div class="col-xs-12 col-sm-6">
        <ul class="list-group">
            <li
                    class="list-group-item"
					v-for="server in servers"
					@click="serverSelected(server)"
                    >
                Server #{{ server.id }}: {{server.status}}
            </li>
        </ul>
    </div>
</template>

<script>

	export default {
		data: function(){
			return {
				servers: [
					{id:1, status: "Normal"},
					{id:2, status: "Critical"},
					{id:3, status: "Bad"},
					{id:4, status: "Okay"},
				]
				
			}
		},
		methods: {
			serverSelected(server){
				this.$emit('serverWasSelected', server);
			}
		}
	}

</script>

<style>

</style>
