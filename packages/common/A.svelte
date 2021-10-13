<a
  use:forwardEvents
  {href}
  {...exclude($$props, ['use', 'href'])}>
  <slot></slot>
</a>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@smui/common/exclude.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let href = 'javascript:void(0);';
</script>
