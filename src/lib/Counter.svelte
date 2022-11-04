<script>
  var count = 0
  const increment = () => {
    count += 1;
  }
  const decrease=()=>{
    count-=1;
  }
</script>

<h3>COUNT IS : {count}</h3>

<button on:click={increment}>
  Increase
</button>

<button on:click={decrease}>Decrease</button>
