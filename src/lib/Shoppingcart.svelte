<script>
    var things=""; let idd=1;
    var thingarr=[];
    const addthing=()=>{
        thingarr=[...thingarr, {id:idd, thing:things}];
        things="";
        idd++;
    }
    const remove=(id2)=>{
        console.log(id2);
        

    }
</script>

<div>
    <h3>Add to cart</h3>
    <input type="text" bind:value={things}>
    <input type="button" value="add" on:click={addthing}>

    <p>{things}</p>
    {#each thingarr as ttt}
        <label class="thing_lb">
            {ttt.id}. {ttt.thing}
            <input type="button" value="X" class="btn_remove" on:click={remove(ttt.id)}/>
        </label>
    {/each}
</div>

<style>
    .thing_lb{
        border: 1px solid indianred;
        padding: 10px;
        margin: 5px;
    }
    .btn_remove{
        border: 1px solid transparent;
    }


</style>