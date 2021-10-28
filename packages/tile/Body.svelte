<div
  use:useActions={use}
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
import {exclude} from '@soddk/common/exclude.js';
import {useActions} from '@soddk/common/useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let image;
</script>
