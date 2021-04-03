<script>
	import { createEventDispatcher, onDestroy } from 'svelte';

	const dispatch = createEventDispatcher();
	const close = () => dispatch('close');

	let modal;

	const handle_keydown = e => {
		if (e.key === 'Escape') {
			close();
			return;
		}

		if (e.key === 'Tab') {
			// trap focus
			const nodes = modal.querySelectorAll('*');
			const tabbable = Array.from(nodes).filter(n => n.tabIndex >= 0);

			let index = tabbable.indexOf(document.activeElement);
			if (index === -1 && e.shiftKey) index = 0;

			index += tabbable.length + (e.shiftKey ? -1 : 1);
			index %= tabbable.length;

			tabbable[index].focus();
			e.preventDefault();
		}
	};

	const previously_focused = typeof document !== 'undefined' && document.activeElement;

	if (previously_focused) {
		onDestroy(() => {
			previously_focused.focus();
		});
	}
</script>

<svelte:window on:keydown={handle_keydown}/>

<div class="modal-background" on:click={close}></div>

<div class="modal" role="dialog" aria-modal="true" bind:this={modal}>
	<slot name="header"></slot>
	<slot></slot>
	<div class="modal-btn-flex">
		<button autofocus on:click={close}><span>Reveal answer</span><i class="fa fa-repeat" aria-hidden="true"></i></button>
	</div>
</div>

<style>
	.modal-background {
		position: fixed;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		background: rgba(0,0,0,0.3);
	}

	.modal {
		position: absolute;
		left: 50%;
		top: 50%;
		transform: translate(-50%,-50%);
		padding: 1em;
		border-radius: 30px;
		background: white;
	}

	button {
		width: 211px;
		height: 45px;
		display: block;
		border: 2px solid var(--unnamed-color-126deb);
		background: #FFFFFF 0% 0% no-repeat padding-box;
		border: 2px solid #126DEB;
		border-radius: 13px;
		opacity: 1;
	}
	button i {
		padding-left: 10px;
	}
	button span {
		color: var(--unnamed-color-126deb);
		text-align: left;
		font: normal normal 600 16px/22px Open Sans;
		letter-spacing: 0px;
		color: #126DEB;
		opacity: 1;
		padding-top: 11px;
		padding-bottom: 12px;
	}
	.modal-btn-flex {
		display: flex;
		justify-content: center;
	}
</style>