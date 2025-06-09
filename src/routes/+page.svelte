<script>
  import { slide } from 'svelte/transition';
  import { dishes } from '$lib/recipes.js'


  let selected = dishes[0];

  function goToTop() {
    document.body.scrollIntoView()
  }

</script>


<svelte:head>
	<title>Eat thru New Orleans</title>
</svelte:head>

<div class="container">

  <h1 style="display:inline-block;">How To Eat Your Way Through</h1>
  <img src="new-orleans-tile.png" class="tile-img" alt="New Orleans"/>

<h2>New Orleans is the number <em>ONE</em> food city in the world according to 
    <a href="https://www.timeout.com/travel/worlds-best-cities-for-food">these guys</a></h2>
    <h2> Check out the following recipes and you will see why</h2>
  <div class="tabs">
    {#each dishes as dish}
      <button type="button"
        class="tab {selected.name === dish.name ? 'active' : ''}"
        onclick={() => { selected = dish }}>
       {dish.name}
      </button>
    {/each}
  </div>



  <div class="centered-div">
    <h2>{selected.name}</h2>
    <input type="checkbox" name="" id="zoom_img">
    <label for="zoom_img">
      <img src={selected.image} class="recipe-img" alt={selected.name} title={selected.title}/>
    </label>
    <div>
        <pre>{selected.name}<br><br>{selected.recipe}</pre>
    </div>
    <button type="button" class="tab"onclick={goToTop}>Go Back To The Top</button>
  </div>
</div>

<style>
  .container {
    max-width: 960px;
    margin: auto;
    padding: 2rem;
    background: linear-gradient(135deg, #fdfcfb 0%, #e2d1c3 100%);
    border-radius: 1rem;
    /* box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1); */
    box-shadow: var(--shadow-elevation-medium);
  }
  button {
    font-family: inherit;
    font-size: 1rem;
    font-weight: 800;
    border-color: #b497d5;
    border-style: solid;
    color: #000000;
    /* These are for responsiveness: */
    min-width: 1.6cm;
    min-height: 1.6cm;
    padding: 2rem;
  }
  .centered-div {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

  .tabs {
    display: flex;
    flex-wrap: wrap;
    overflow-x: auto;
    gap: 0.5rem;
    padding-bottom: 1rem;
    margin-bottom: 2rem;
    scroll-snap-type: x mandatory;
  }

  .tab {
    white-space: nowrap;
    padding: 0.75rem 1.25rem;
    border-radius: 9999px;
    background-color: #f4f4f5;
    color: #000000;
    cursor: pointer;
    transition: all 0.3s ease;
    scroll-snap-align: start;
    flex-shrink: 0;
  }
  .tab:hover {
    background-color: #e0e0e0;
  }
  .tab.active {
    background-color: #b497d5;
    color: white;
    font-weight: bold;
  }
  img {
    display: block;
    max-width: 100%;
    transition: 1s;
  }
  img:hover {
    cursor: zoom-in;
  }
  input[type=checkbox] {
    display: none;
  }
  input[type=checkbox]:checked ~ label > img {
    transform: scale(1.5);
    cursor: zoom-out;
  }
  .tile-img {
    display: inline-block;
    margin-bottom: -.75rem;
    /* box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1); */
    box-shadow: var(--shadow-elevation-medium);

  }
  .recipe-img {
    max-width: 100%;
    border-radius: 1.5rem;
    /* box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
     */
    box-shadow: var(--shadow-elevation-medium);
    margin-bottom: 1.5rem;
    -ms-interpolation-mode: bicubic;
    vertical-align: bottom;
    justify-content: center;
    align-items: center;
    text-align: center;
  }
  pre {
    white-space: pre-wrap;
    font-family: 'Courier New', monospace;
    background-color: #fff7ed;
    padding: 1.25rem;
    border-left: 4px solid #147A19;
    border-right: 4px solid #b497d5;
    border-radius: 0.5rem;
    /* box-shadow: inset 0 1px 3px rgba(0,0,0,0.05); */
        box-shadow: var(--shadow-elevation-medium);

    overflow-x: auto;
    cursor: text;
  }

  @media (max-width: 768px) {
    .container {
      padding: 1rem;
      border-radius: 0.75rem;
    }

    .tabs {
      /* display: none; */
      display: flex;
    }

    .tab {
      padding: 0.5rem 1rem;
      font-size: 0.875rem;
    }
    h1 {
      font-size: 2rem;
    }
    h2 {
      font-size: 1.5rem;
    }
    pre {
      font-size: 0.875rem;
    }
  }
</style>
