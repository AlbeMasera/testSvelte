<script lang="ts">
    import Map from '$comp/Map.svelte';
    import Bar from '$comp/Barchart.svelte';
    import Time from '$comp/TimeSelection.svelte';

    const something = {data1:"hello",data2:"world"}

</script>



<div class="grid grid-cols-3 ">
    <div></div>
    <div class="grid grid-rows-3">
        <Time/> 
        
      </div>
    <div class="grid grid-rows-2">
        <Time/>
        <Map/>
      </div>
     
  </div>

  
