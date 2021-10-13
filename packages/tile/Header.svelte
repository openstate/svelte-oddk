<div
  use:forwardEvents
  class="oddk-tile-header" {...exclude($$props, ['use', 'class', 'type'])}>
  <slot></slot>
</div>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@smui/common/exclude.js';

const forwardEvents = forwardEventsBuilder(get_current_component());
</script>
