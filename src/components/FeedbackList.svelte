<script>
    import {FeedbackStore} from '../stores'
    import {onMount,onDestroy} from 'svelte'
    import { each} from "svelte/internal";
    import {fade, scale} from 'svelte/transition'
    import FeedbackItem from "./FeedbackItem.svelte";

     
    
</script>

{#each $FeedbackStore as fb (fb.id)}
    <div in:scale out:fade>
        <FeedbackItem item={fb}/>
    </div>
{/each}