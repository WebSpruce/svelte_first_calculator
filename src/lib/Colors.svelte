<script>
    var random = 0;
    var chars_arr=['0','1','2','3','4','5','6','7','8','9','A','B','C','D','E','F'];
    var randomcolor="#";
    const randomstart=()=>{
        let min=Math.ceil(1);
        let max=Math.ceil(100);
        random = Math.floor(Math.random()*(max-min)+min);
    }
    const randomstart2=()=>{
        randomcolor="#";
        for(let i=0; i<6; i++){
            let id=Math.floor(Math.random()*16);
            randomcolor+=chars_arr[id];
        }
    }
</script>

<h3>random number : {random}</h3>
<div style="background-color: {randomcolor}; padding:10px">
    <label>{randomcolor}</label>
</div>
<input type="button" on:click={randomstart} value="generate random number"/><br>
<input type="button" on:click={randomstart2} value="generate random color"/>

<style>

</style>