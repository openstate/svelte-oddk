<a
  use:useActions={use}
  use:forwardEvents
  {href}
  class="oddk-tile-action"
  {alt}
  {...exclude($$props, ['use', 'href', 'alt'])}>
  <slot></slot>
</a>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@soddk/common/exclude.js';
import {useActions} from '@soddk/common/useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let href = 'javascript:void(0);'
export let alt = "Home";
</script>
