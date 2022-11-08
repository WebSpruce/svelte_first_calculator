<script>
    var random = 0;
    const randomstart=()=>{
        let min=Math.ceil(1);
        let max=Math.ceil(100);
        random = Math.floor(Math.random()*(max-min)+min);
    }
</script>

<h3>random number : {random}</h3>
<input type="button" on:click={randomstart} value="generate random number"/>