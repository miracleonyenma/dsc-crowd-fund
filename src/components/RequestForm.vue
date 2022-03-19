<template>
	<form>
		<div class="wrapper">
			<header class="mb-6">
				<div class="wrapper">
					<h2 class="font-bold text-3xl">Fund Request Form</h2>
					<p>Only one more step to get started, fill the form below!</p>
				</div>
			</header>
			<div class="form-control">
				<label for="name">
					<span>Name</span>
					<input id="name" type="text" name="name" class="rounded-lg" placeholder="Enter you name " required />
				</label>
			</div>
			<div class="form-control">
				<label for="title">
					<span>Fund Request</span>
					<input
						id="title"
						type="text"
						name="title"
						class="rounded-lg"
						placeholder="What do you want to call this request"
						required
					/>
				</label>
			</div>
			<div class="form-control">
				<label for="amount">
					<span>Your Amount</span>
					<input
						id="amount"
						type="number"
						name="amount"
						class="rounded-lg"
						placeholder="Enter your desired amount"
						required
					/>
				</label>
			</div>
			<div class="form-control">
				<label for="description">
					<span>Fund Description</span>
					<textarea
						name="description"
						id="description"
						cols="10"
						rows="2"
						class="rounded-lg"
						placeholder="Enter a short description for your request"
					></textarea>
				</label>
			</div>
			<div class="form-control">
				<label for="formFile" class="form-label inline-block mb-2 text-gray-700">
					<span>Upload file</span>

					<input
						class="block w-full text-sm bg-gray-50 rounded-lg border border-gray-300 cursor-pointer file:bg-purple-600 file:text-purple-50 file:border-none file:p-2"
						aria-describedby="user_avatar_help"
						id="user_avatar"
						type="file"
					/>
					<div class="mt-1 text-sm text-slate-500">Upload fund request image/proof</div>
				</label>
			</div>

			<div class="action-cont pt-1">
				<button class="cta">Submit Request</button>
			</div>
		</div>
	</form>
</template>

<style scoped>
	form {
		@apply pt-4 px-4;
	}
	form > .wrapper {
		@apply bg-white p-6 min-h-[calc(100vh-12rem)] max-h-screen overflow-y-auto rounded-t-xl;
	}

	.form-control label {
		@apply flex flex-col gap-1 mb-3;
	}
</style>
