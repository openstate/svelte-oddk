<div
  use:forwardEvents
  class="oddk-tile oddk-tile-{type}" {...exclude($$props, ['use', 'class', 'type', 'byline'])}>
</div>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@smui/common/exclude.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let type = "person";
export let avatar = type + ".svg";
export let byline = '';
</script>
