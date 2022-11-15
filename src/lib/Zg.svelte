<script>
    let word = ""; let word2=""; let index = 0; let result=""; let f=0; let guess=false;
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
    const guessfunction=(e)=>{
        function replaceChar(origString, replaceChar, index)
        {
            let firstPart = origString.substr(0, index);
            let lastPart = origString.substr(index + 1);
            let newString =
                firstPart + replaceChar + lastPart;
            return newString;
        }

        if(e.key==='Enter'){
            console.log("E : "+e.target.value);
            for(let i=0; i<word.length; i++){

                if(e.target.value == word[i]){
                    console.log("OK : "+e.target.value);
                    word2=replaceChar(word2,e.target.value,i);
                    guess=true;
                }
            }
            console.log("guess: "+guess);
            if(guess==false){
                f++;
            }


            e.target.value="";
            if(!word2.includes("*")){
                console.log("YES!");
                result="YOU WON!";
            }

        }

    }
    const reset=()=>{
        result="";
        word2="";
        generaterandom();
    }
</script>

<h3>Word: {word2}</h3>
<h6>f: {f}</h6>

<input type="button" value="generate word" on:click={generaterandom}>

<input type="text" maxlength="1" on:keydown={guessfunction}>
<h3>{result}</h3>
<input type="button" value="reset" on:click={reset}>

<style>
    h6{
        color:indianred;
    }
</style>