<script>
    let result=0, n1=0, n2=0; let selection="";
    const changeselection=(e)=>{
        selection=e.target.value;
        console.log("selection: "+selection);
    }
    const calculate=()=>{
        if(selection=="a"){
            result=n1+n2;
            console.log("n1: "+n1+" , n2: "+n2);
        }else if(selection=="s"){
            result=n1-n2;
        }else if(selection=="m"){
            result=n1*n2;
        }else if(selection=="d"){
            if(n2!=0){
                result=n1/n2;
            }else{
                alert("n2 is 0");
            }
            
        }
    }
</script>

<h2>RESULT : {result.toFixed(2)}</h2>
<input type="number" placeholder="num 1" bind:value={n1}>
<input type="number" placeholder="num 2" bind:value={n2}><br><br>
    addition: <input type="radio" name="operations" on:change={changeselection} value="a"><br>
    substraction: <input type="radio" name="operations" on:change={changeselection} value="s"><br>
    multiplication: <input type="radio" name="operations" on:change={changeselection} value="m"><br>
    division: <input type="radio" name="operations" on:change={changeselection} value="d"><br><br>
<input type="button" value="CALCULATE" on:click={calculate}>

<style>
    input{
      border:3px solid indianred;
      color:white;
      padding:10px;
    }
  </style>