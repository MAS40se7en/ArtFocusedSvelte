<script lang="ts">
	import { EnvelopeClosed } from "svelte-radix";
    


    const dropOptions = [
        {
            icon:EnvelopeClosed,
            title: Notification,
            href: '/'
        }
    ]
</script>

<div>
    <a href="/"><EnvelopeClosed/></a>
    <a href="/">Posts</a>
    <a href="/">Logout</a>
</div>