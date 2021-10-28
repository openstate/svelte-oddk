<a
use:useActions={use}
use:forwardEvents
{href}
class="oddk-menubar-logo"
{alt}
{...exclude($$props, ['use', 'href', 'alt', 'src'])}>
  <img {src} alt="logo" class="oddk-logo">
</a>

<script>
import {get_current_component} from 'svelte/internal';
import {forwardEventsBuilder} from '@soddk/common/forwardEvents.js';
import {exclude} from '@soddk/common/exclude.js';
import {useActions} from '@soddk/common/useActions.js';

const forwardEvents = forwardEventsBuilder(get_current_component());

export let use = [];
export let href = "/";
export let alt = "Home";
export let src = "/images/oddk/logo.svg";
</script>
