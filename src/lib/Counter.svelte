<script>
  let count = $state(0)
  const increment = () => {
    count += 1
  }
</script>

<button class="btn" onclick={increment}>
  count is {count}
</button>
<div>hello my svelte app is running</div>


<style>
  /* Add your CSS styles here */
 .btn {
  background-color: #4CAF50;
  color: white;
  padding: 10px 20px;
 }
</style>