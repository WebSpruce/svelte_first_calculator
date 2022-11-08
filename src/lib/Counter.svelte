<script>
  var count = 0
  const increment = () => {
    count += 1;
  }
  const decrease=()=>{
    count-=1;
  }
  const reset=()=>{
    count=0;
  }
</script>

<h3>COUNT IS : {count}</h3>

<button on:click={increment}>
  Increase
</button>

<button on:click={decrease}>Decrease</button>
<button on:click={reset}>Reset</button>
