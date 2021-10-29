<h2
  use:useActions={use}
  use:forwardEvents
  class={h2_class}
  {...exclude($$props, ['use', 'class'])}>
  <slot></slot>
</h2>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from './forwardEvents.js';
import {exclude} from './exclude.js';
import {useActions} from './useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let variant = "normal";
let h2_class = "oddk-h2-" + variant;
</script>
