<script>
	import { getData, getDrive } from "../data";
	import { Filemanager } from "../../src";
</script>

{#snippet folderSuffix(folder)}
	<div class="folder-suffix">
		{folder.open ? "Open" : "Closed"}
	</div>
{/snippet}

<Filemanager data={getData()} drive={getDrive()} {folderSuffix} />

<style>
	.folder-suffix {
		color: blue;
		background-color: #fff;
		border: 1px solid #a6a6a6;
		box-shadow: 0 0 10px 0 rgba(0, 0, 0, 0.1);
		border-radius: 8px;
		padding: 2px;
		font-size: 10px;
	}
</style>
