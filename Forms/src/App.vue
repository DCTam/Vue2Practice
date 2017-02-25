<template>
    <div class="container">
        <form>
            <div class="row">
                <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                    <!-- Exercise 1 -->
                    <!-- Create a Signup Form where you retrieve the following Information -->
                    <!-- Full Name (First Name + Last Name) -->
                    <!-- Mail -->
                    <!-- Password -->
                    <!-- Store Data? Yes/No -->
					<form>
						<form-group>
							<label>Name</label>
							<input type="text" class="form-control" v-model="name">
							<label>Mail</label>
							<input type="text" class="form-control" v-model="mail">
							<label>Password</label>
							<input type="password" class="form-control" v-model="password">
							<label>Store data?</label> <br>
							Yes: <input type="radio" value="true" v-model="store"> <br>
							No: <input type="radio" value="false" v-model="store"> <br>
							<button class="btn btn-primary" @click.prevent="display = true">Submit</button>
						</form-group>
					</form>

                    <!-- Exercise 2 -->
                    <!-- Only display the Form if it has NOT been submitted -->
                    <!-- Display the Data Summary ONCE the Form HAS been submitted -->

                    <!-- Exercise 3 -->
                    <!-- Edit the Example from above and create a custom "Full Name" Control -->
                    <!-- which still holds the First Name and Last Name Input Field -->
                </div>
            </div>
        </form>
        <hr>
        <div class="row">
            <div class="col-xs-12 col-sm-8 col-sm-offset-2 col-md-6 col-md-offset-3">
                <div class="panel panel-default" v-if="display">
                    <div class="panel-heading">
                        <h4>Your Data</h4>
                    </div>
                    <div class="panel-body">
                        <p>Full Name: {{name}}</p>
                        <p>Mail: {{mail}}</p>
                        <p>Password: {{password}}</p>
                        <p>Store in Database?: {{store}}</p>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    export default {
		data(){
			return {
				display: false,
				name: '',
				password: '',
				mail: '',
				store: false
			}
		}
    }
</script>

<style>
</style>
