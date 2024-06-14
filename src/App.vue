<script>
export default {
	data() {
		return {
			formValues: {
				name: "",
				summary: "",
				country: "",
				jobLoction: [],
				jobRemote: false,
				skillSet: [],
				yearsOfExperience: ''
			},
		};
	},
	methods: {
		submitForm(event){
event.preventDefault()
console.log('Form Value is', this.formValues);
		}
	},
};
</script>

<template>
	<div>
		<pre>
        {{ JSON.stringify(formValues, null, 1) }}
    </pre>
	</div>
	<form @submit="submitForm">
		<div>
			<label for="name">Name : </label>
			<input id="name" type="text" v-model="formValues.name" />
		</div>

		<div>
			<label for="summary">Summary : </label>
			<input id="summary" type="text" v-model="formValues.summary" />
		</div>

		<div>
			<label for="country">Country : </label>
			<select id="country" v-model="formValues.country">
				<option value="">Select a country</option>
				<option value="india">India</option>
				<option value="vietnam">Vietnam</option>
				<option value="singapore">Singapore</option>
			</select>
		</div>

		<div>
			<label for="job-location">Job Location : </label>
			<select id="job-location" multiple v-model="formValues.jobLoction">
				<option value="india">India</option>
				<option value="vietnam">Vietnam</option>
				<option value="singapore">Singapore</option>
			</select>
		</div>

		<div>
			<input type="checkbox" id="jobRemote" v-model="formValues.jobRemote" true-value="yes" false-value="no" />
			<label for="jobRemote">Open to remote work ?</label>
		</div>

		<div>
			<label>Skill Set :</label>
			<input type="checkbox" id="html" value="html" v-model="formValues.skillSet" />
			<label for="html">HTML</label>
			<input type="checkbox" id="js" value="js" v-model="formValues.skillSet" />
			<label for="js">JS</label>
			<input type="checkbox" id="css" value="css" v-model="formValues.skillSet" />
			<label for="css">CSS</label>
		</div>

		<div>
			<label>Years of Experience :</label>
			<input type="radio" id="0-2" value="0-2" v-model="formValues.yearsOfExperience" />
			<label for="0-2">0-2</label>
			<input type="radio" id="2-4" value="2-4" v-model="formValues.yearsOfExperience" />
			<label for="2-4">2-4</label>
			<input type="radio" id="4-6" value="4-6" v-model="formValues.yearsOfExperience" />
			<label for="4-6">4-6</label>
			<input type="radio" id="6-8" value="6-8" v-model="formValues.yearsOfExperience" />
			<label for="6-8">6-8</label>
		</div>

		<div>
			<button>Submit</button>
		</div>
	</form>
</template>

<style></style>
