<script>
	export let name;

  let todoAry=[]
  let Name =""

  const handleSubmit=(e)=>{
    e.preventDefault();
    todoAry.push(Name)
    console.log(todoAry);
    Name=""
     todoAry = todoAry
  }
</script>

<main> 
	<div class="mx-0" >Logo <span class="float-right btn" >Nav</span></div>

  <div class="d-flex align-items-center justify-content-center flex-column mt-5 mx-5" >
    <h2>Today</h2>
    <form on:submit={handleSubmit} >
      <input class="form-control" value={Name} type="text" placeholder="What's in your mind?" on:change={(e)=> Name= e.target.value} />
    </form>
  </div>


<p>
  {#each todoAry as item}
  <li>{item}</li>
{/each}
</p>
</main>

<style>
	main {
		
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>