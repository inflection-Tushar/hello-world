<script>
  import { createEventDispatcher } from "svelte";

    const dispatch=createEventDispatcher()
    function eventclicked(){
        dispatch('hi',{
            text:"hello"
        })
        // alert("event is clicked..")
    }
</script>
<button on:click={eventclicked}>click me</button>