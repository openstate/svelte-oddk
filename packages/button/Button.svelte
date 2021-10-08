<a {href}
  use:forwardEvents
  class="
    oddk-button
    {className}
    {variant === 'normal' ? 'oddk-button-normal' : ''}
    {variant === 'raised' ? 'oddk-button-raised' : ''}
    {variant === 'cta' ? 'oddk-button-cta' : ''}
  "
  {...exclude($$props, ['use', 'class', 'variant', ...dialogExcludes])}
><slot></slot></a>

<script>
  import {get_current_component} from 'svelte/internal';
  import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
  import {exclude} from '@smui/common/exclude.js'; // TODO: uhm, need to factor this out`

  const forwardEvents = forwardEventsBuilder(get_current_component());

  let dialogExcludes = [];
  let className = '';
  export let use = [];
  export {className as class};
  export let variant = 'normal';
  export let href = 'javascript:void(0);';
</script>
