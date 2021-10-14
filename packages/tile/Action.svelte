<a {href}
  use:forwardEvents
  class="oddk-tile-action" {...exclude($$props, ['use', 'class'])}>
  <slot></slot>
</a>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@smui/common/exclude.js';
import A from '@soddk/common/A.svelte';
import Button from '@soddk/button/';

const forwardEvents = forwardEventsBuilder(get_current_component());
export let href = 'javascript:void(0);'
</script>
