<script>
    let name="Sven";
    let operators=[{op:'h1',color:'red'},{op:'h2',color:'green'},{op:'h3',color:'blue'},{op:'h4',color:'purple'},{op:'h5',color:'yellow'}];
    let selected=operators[0];
</script>

<input type="text" bind:value={name}>
<select bind:value={selected}>
    {#each operators as option}
        <option value="{option}">{option.op}</option>
    {/each}
</select>
<svelte:element this="{selected.op}" style="color:{selected.color}">{selected.op} - welcome {name}</svelte:element>