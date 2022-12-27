<script>
    import { FeedbackStore } from "../stores";
    $:count=$FeedbackStore.length
    $:average=($FeedbackStore.reduce((a,{rating})=>a+rating,0)/$FeedbackStore.length).toFixed(1)
	
    
    

</script>

<div class="feedback-stats">
    <h4>{count} Reviews</h4>
    {#if count==0}
        <h4>Rating Average : There is no Reviews</h4>
    {:else}
        <h4>Rating Average : {average}</h4>   
    {/if}
</div>


<style>
    .feedback-stats{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
</style>