<div class="oddk-profile oddk-profile-{type}" {...exclude($$props, ['use', 'class', 'type', 'byline'])}>
  <img src="/images/oddk/{avatar}" class="oddk-profile-avatar" />
  <div class="oddk-profile-details">
    <slot></slot>
    {#if byline}
    <div class="oddk-profile-byline">{byline}</div>
    {/if}
  </div>
</div>

<script>
import {exclude} from '@smui/common/exclude.js';

export let type = "person";
export let avatar = type + ".svg";
export let byline = '';
</script>
