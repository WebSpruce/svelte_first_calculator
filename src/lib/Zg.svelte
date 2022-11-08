<script>
    let word = ""; let word2=""; let index = 0;
    const generaterandom=()=>{
        let words=["banana","apple","orange","melon","pumpkin"];
        let min = Math.ceil(0);
        let max = Math.floor(4);
        index = Math.floor(Math.random() * (max - min) + min);

        word=words[index];
        for(let i=0; i<word.length; i++){
            word2+="*";
        }
    }
</script>

<h3>Word: {word2}</h3>

<input type="button" value="generate word" on:click={generaterandom}>

<input type="text" on:keydown={e=>{if(e.target.value )}}>