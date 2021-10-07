<button {href}
  this={component}
  class="
    oddk-button
    {className}
    {variant === 'normal' ? 'oddk-button-normal' : ''}
    {variant === 'raised' ? 'oddk-button-raised' : ''}
    {variant === 'cta' ? 'oddk-button-cta' : ''}
  "
  {...exclude($$props, ['use', 'class', 'variant', ...dialogExcludes])}
><slot></slot></button>

<script>
  import {exclude} from '@smui/common/exclude.js';

  let dialogExcludes = [];
  let className = '';
  export {className as class};
  export let variant = 'normal';
  export let href = null;
  export let component;
</script>
