<a {href}
  this={component}
  class="
    oddk-button
    {className}
    {variant === 'raised' ? 'oddk-button-raised' : ''}
    {variant === 'cta' ? 'oddk-button-cta' : ''}
  "
  {...exclude($$props, ['use', 'class', 'variant', ...dialogExcludes])}
><slot></slot></a>

<script>
  import {exclude} from '@smui/common/exclude.js';

  let dialogExcludes = [];
  let className = '';
  export {className as class};
  export let variant = 'text';
  export let href = null;
  export let component;
</script>
