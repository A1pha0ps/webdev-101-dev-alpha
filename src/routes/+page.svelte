<script>
	import { currentUser } from '$lib/pocketbase';

	let caption = '';
</script>

kevin

{#if $currentUser}
	<div class="flex justify-center">
		<!-- The button to open modal -->
		<label for="my-modal-4" class="btn-primary btn">Create Post</label>

		<!-- Put this part before </body> tag -->
		<input type="checkbox" id="my-modal-4" class="modal-toggle" />
		<label for="my-modal-4" class="modal cursor-pointer">
			<label class="modal-box relative" for="">
				<div class="space-y-4">
					<h3 class="text-lg font-bold">Create Post!</h3>
					<div class="form-control">
						<label class="label">
							<span class="label-text">Caption</span>
						</label>

						<textarea class="textarea-bordered textarea h-24" bind:value={caption} />
					</div>
					<input type="file" class="file-input-bordered file-input w-full max-w-xs" />
					<button class="btn-primary btn-block btn">Create post</button>
				</div>
			</label>
		</label>
	</div>
{/if}
