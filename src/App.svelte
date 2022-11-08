<script>
  import Calculator from './lib/Calculator.svelte';
  import Calculator2 from './lib/Calculator2.svelte';
  import Counter from './lib/Counter.svelte'
  import Colors from "./lib/Colors.svelte";
  import Shoppingcart from "./lib/Shoppingcart.svelte";
  import Zg from "./lib/Zg.svelte";
</script>

<main>

  <div class="card">
    <Counter />
  </div>

  <div class="card">
    <Calculator/>
  </div>

  <div class="card">
    <Calculator2/>
  </div>
  <div class="card">
    <Colors/>
  </div>
  <div class="card">
    <Shoppingcart></Shoppingcart>
  </div>
  <div class="card">
    <Zg></Zg>
  </div>
</main>

<style>
  div{
    border:3px solid indianred;
      color:white;
      padding:10px;
  }
</style>
