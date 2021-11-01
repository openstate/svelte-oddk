<a
  use:useActions={use}
  use:forwardEvents
  {href}
  class="oddk-tag oddk-tag-{variant}"
  {...exclude($$props, ['use', 'href'])}>
  <slot></slot>
</a>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from './forwardEvents.js';
import {exclude} from './exclude.js';
import {useActions} from './useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let href = 'javascript:void(0);';
export let variant = 'normal';
</script>
