<div
  use:forwardEvents
  class="oddk-tile-body" {...exclude($$props, ['use', 'class', 'type'])}>
  <slot></slot>
  {#if image}
  <img class="oddk-tile-image" src="https://via.placeholder.com/250x170">
  {/if}
</div>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@smui/common/exclude.js';

export let image;

const forwardEvents = forwardEventsBuilder(get_current_component());
</script>
