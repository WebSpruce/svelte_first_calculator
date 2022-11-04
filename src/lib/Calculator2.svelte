<script>
    let selection="";
    let numbers=[0]; let nn=0; let sum=0; let op=""; var st="";
    var color="";
    const GetValue=(e)=>{
        nn=e.target.value;
        console.log("value: "+nn);
    }

    const changeselection=(e)=>{
        selection=e.target.value;
    }
    const reset=()=>{
        numbers=[];
        sum=0;
        st="0";
    }
    
    const calculate=()=>{
        if(selection=="+"){
            numbers=[...numbers, nn];
            sum+=Number(nn);
            op="+";
        }else if(selection=="-"){
            numbers=[...numbers, nn];
            sum-=Number(nn);
            op="-";
        }else if(selection=="*"){
            numbers=[...numbers, nn];
            sum*=Number(nn);
            op="*";
        }else if(selection=="/"){
            if(nn!=0){
                numbers=[...numbers, nn];
                sum/=Number(nn);
                op="/";
            }else{
                alert("n2 is 0");
            }
        }
        var ch=[]; var ch2=[]; let short="";
        ch.push(numbers[numbers.length-2]);
        ch.push(numbers[numbers.length-1]);
        console.log("ccch: "+ch.join(" "+op+" "));
        
        st+=" | "+ch.join(" "+op+" ");

        color="red";
    }
    
    
    
</script>

<h2>{st} = {sum.toFixed(2)}</h2>
    <form>
        <input type="button" value="1" on:click={GetValue}>
        <input type="button" value="2" on:click={GetValue}>
        <input type="button" value="3" on:click={GetValue}><br>
        <input type="button" value="4" on:click={GetValue}>
        <input type="button" value="5" on:click={GetValue}>
        <input type="button" value="6" on:click={GetValue}><br>
        <input type="button" value="7" on:click={GetValue}>
        <input type="button" value="8" on:click={GetValue}>
        <input type="button" value="9" on:click={GetValue}><br>
    </form>
<br>
    <input type="button" name="operations" on:click={changeselection} value="+">
    <input type="button" name="operations" on:click={changeselection} value="-">
    <input type="button" name="operations" on:click={changeselection} value="*">
    <input type="button" name="operations" on:click={changeselection} value="/"><br><br>
<input type="button" value="CALCULATE" on:click={calculate} style="background-color: {color}">
<input type="button" value="RESET" on:click={reset}>

<style>
    input{
      border:3px solid indianred;
      color:white;
      padding:10px;
      margin:5px 0px 0px 0px;
    }
    input:hover{
        background-color: gainsboro;
    }
    input:active{
        border:5px solid indianred;
    }
  </style>