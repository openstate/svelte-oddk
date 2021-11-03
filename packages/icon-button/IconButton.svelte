<a
  use:useActions={use}
  use:forwardEvents
  {href}
  class="
    oddk-icon-button
    {className}
    {variant === 'normal' ? 'oddk-button-normal' : ''}
    {variant === 'raised' ? 'oddk-button-raised' : ''}
    {variant === 'cta' ? 'oddk-button-cta' : ''}
  "
  {...exclude($$props, ['href', 'use', 'class', 'variant', ...dialogExcludes])}
><slot></slot></a>

<script>
  import {get_current_component} from 'svelte/internal';
  import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
  import {exclude} from '@soddk/common/exclude.js';
  import {useActions} from '@soddk/common/useActions.js';

  const forwardEvents = forwardEventsBuilder(get_current_component());

  let dialogExcludes = [];
  let className = '';
  export let use = [];
  export {className as class};
  export let variant = 'normal';
  export let href = 'javascript:void(0);';
</script>
