<div
  use:useActions={use}
  use:forwardEvents
  class="oddk-profile oddk-profile-{type}" {...exclude($$props, ['use', 'class', 'type', 'byline'])}>
  <img src="/images/oddk/{avatar}" class="oddk-profile-avatar" />
  <div class="oddk-profile-details">
    <slot></slot>
    {#if byline}
    <div class="oddk-profile-byline">{byline}</div>
    {/if}
  </div>
</div>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from './forwardEvents.js';
import {exclude} from './exclude.js';
import {useActions} from './useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let type = "person";
export let avatar = type + ".svg";
export let byline = '';
</script>
