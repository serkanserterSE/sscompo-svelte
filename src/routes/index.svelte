<script>
	import BoxGroup from "../components/box/boxGroup.svelte";
	import Box from "../components/box/box.svelte";
	import Modal from "../components/modal/modal.svelte";
import Pagination from "../components/pagination/pagination.svelte";
	let isOpenModal = false;
</script>

<svelte:head>
	<title>SSCOMPO-SVELTE</title>
	<meta name="description" content="Svelte Components" />
</svelte:head>
<div style="height: 100px;">
	<Pagination pageCount={10}></Pagination>
</div>
<div style="height: 100px;">
	<button on:click={() => (isOpenModal = !isOpenModal)}>Open Modal</button>
	<Modal
		bind:isOpen={isOpenModal}
		title="Modal - Lorem ipsum dolor sit amet"
		iconUrl="http://localhost:3000/favicon.png"
	>
		<div slot="content">
			<em>
				Donec id magna blandit felis tincidunt porta. Donec vel enim
				nisi. Aenean egestas sem id interdum lacinia. Nullam
				sollicitudin, nulla nec tincidunt suscipit, risus purus luctus
				ipsum, at sodales velit lacus nec eros. Donec tempus diam at
				nunc euismod placerat. Etiam a eros id ex malesuada suscipit.
			</em> 
		</div>
		<div slot="custom-buttons">
			<button type="button" on:click={() => alert("OK")}>Tamam</button>
		</div>
	</Modal>
</div>

<BoxGroup>
	<Box
		title="Lorem ipsum dolor sit amet"
		iconUrl="http://localhost:3000/favicon.png"
	>
		<span slot="content">
			Donec id magna blandit felis tincidunt porta. Donec vel enim nisi.
			Aenean egestas sem id interdum lacinia. Nullam sollicitudin, nulla
			nec tincidunt suscipit, risus purus luctus ipsum, at sodales velit
			lacus nec eros. Donec tempus diam at nunc euismod placerat. Etiam a
			eros id ex malesuada suscipit. Nullam urna risus, aliquet eu
			scelerisque ac, eleifend at ante. Duis ut libero sed dolor
			sollicitudin vulputate et id quam. Sed sit amet ornare risus.
		</span>
		<span slot="foot">
			Curabitur tempor ex ligula, pretium semper ex dapibus et. Sed
			sodales augue vel ipsum varius, sit amet gravida sapien ultricies</span
		>
	</Box>

	<Box
		title="Lorem ipsum dolor sit amet"
		subtitle="Ut cursus vitae nisi quis elementum"
		width="457px"
	>
		<span slot="content">
			Donec id magna blandit felis tincidunt porta. Donec vel enim nisi.
			Aenean egestas sem id interdum lacinia. Nullam sollicitudin, nulla
			nec tincidunt suscipit, risus purus luctus ipsum, at sodales velit
			lacus nec eros. Donec tempus diam at nunc euismod placerat. Etiam a
			eros id ex malesuada suscipit. Nullam urna risus, aliquet eu
			scelerisque ac, eleifend at ante. Duis ut libero sed dolor
			sollicitudin vulputate et id quam. Sed sit amet ornare risus.
		</span>
	</Box>
	<Box>
		<span slot="content">
			Donec id magna blandit felis tincidunt porta. Donec vel enim nisi.
			Aenean egestas sem id interdum lacinia. Nullam sollicitudin, nulla
			nec tincidunt suscipit, risus purus luctus ipsum, at sodales velit
			lacus nec eros. Donec tempus diam at nunc euismod placerat. Etiam a
			eros id ex malesuada suscipit. Nullam urna risus, aliquet eu
			scelerisque ac, eleifend at ante. Duis ut libero sed dolor
			sollicitudin vulputate et id quam. Sed sit amet ornare risus.
		</span>
		<div slot="foot">
			Curabitur tempor ex ligula, pretium semper ex dapibus et. Sed
			sodales augue vel ipsum varius, sit amet gravida sapien ultricies
		</div>
	</Box>
	<Box>
		<div slot="content">
			Donec id magna blandit felis tincidunt porta. Donec vel enim nisi.
			Aenean egestas sem id interdum lacinia. Nullam sollicitudin, nulla
			nec tincidunt suscipit, risus purus luctus ipsum, at sodales velit
			lacus nec eros. Donec tempus diam at nunc euismod placerat. Etiam a
			eros id ex malesuada suscipit. Nullam urna risus, aliquet eu
			scelerisque ac, eleifend at ante. Duis ut libero sed dolor
			sollicitudin vulputate et id quam. Sed sit amet ornare risus.
		</div>
	</Box>
</BoxGroup>
