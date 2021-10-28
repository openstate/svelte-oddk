<div
  use:useActions={use}
  use:forwardEvents
  class="oddk-menubar-items"
  {...exclude($$props, ['use', 'class'])}>
  <slot></slot>
</div>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@soddk/common/exclude.js';
import {useActions} from '@soddk/common/useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
</script>
