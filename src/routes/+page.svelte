<script>
  import { slide } from 'svelte/transition';

  export let dishes = [
    {
      name: "Corn and Crab Claw Bisque",
      image: "/corn-crab-bisque.png",
      recipe: `Serves six people and takes about an hour to make.
Ingredients:
1⁄2 cup flour.
1⁄2 cup butter.
1 quart heavy cream, warm to room temperature.
1 quart chicken stock.
3 tablespoons cajun seasoning, to-taste.
2 garlic cloves, minced.
3 tablespoons garlic, dehydrated flakes
1 twig thyme (dried is ok)
1 twig rosemary (optional)
1⁄2 lb crabmeat (claw)
24 ounces corn, with liquid (frozen is ok)
2 tablespoons clove crab boil seasoning (liquid)
1 cup green onion, chopped
1 tablespoon parsley, chopped

Cooking Instructions:
1. In a sauté pan, make the blonde roux first. Melt butter on low-medium heat, then add flour and wisk continuosly for about 10 minutes until it starts to turn light blonde color and smells a little 'nutty'. Time may vary; it's more about the color and smell.
2. Add roux in a cold stock pot to stop the cooking, and add cold chicken stock and corn. Bring to a boil, stirring occasionally. Reduce to simmer, add fresh garlic and garlic flakes, thyme, and rosemary (if desired). Simmer for 10-12 minutes.
3. Add cream, crab, cajun seasoning, crab boil seasoning. Simmer another 10 minutes.
4. Add half the green onion, and half the parsley, mix and serve. Garnish with remaining green onion and parsley.
5. Optional: can add gouda, cheddar, or blue cheese for a little kick!`
    },
    {
      name: "Shrimp Creole",
      image: "/shrimp-creole.webp",
      recipe: `Serves four people and takes about an hour to make.

Ingredients:

1/4 cup or 1/2 stick of butter
1/4 cup of flour
1 nice onion, diced
a couple of stalks of celery, diced
1/2 of a green bell pepper, diced
1 or 2 toes of garlic, minced
a few pieces of dehydrated garlic, sliced
1 1/2 cups of seafood or chicken or vegetable stock
1 8 oz can of tomato sauce or make your own
1 bay leaf
1/2 tablespoon of brown sugar or Steen's Cane syrup
2 - 3 thin lemon slices
Creole seasoning - to taste, don't be shy
a few sprinkles of dry basil or a few leaves of fresh basil
a few sprinkles of dry thyme or a couple of twigs of picked thyme
1/2 cup of green onions, sliced
1/4 cup of parsley, chopped
1 1/2 pounds of peeled raw shrimp - small ones are tastier
3 cups of cooked rice (so cook 1 1/2 cups of rice)

Cooking Instructions:

1. Melt butter and add flour, stir over medium heat until lightly browned.
2. Sauté onions, bell peppers, celery until soft the onions are transparent.
3. Add the garlic and sauté a bit more (5 minutes).
4. Add the stock, tomato sauce, bay leaf, brown sugar or Steen's syrup, lemon slices, Creole seasoning, basil and thyme.
5. Simmer sauce for 15 minutes, then add shrimp, green onions and parsley.
6. Cook until shrimp are pink, about 3 minutes.
7. Serve over white rice and garnish with green onions and parsley.`
    },
    {
      name: "Bananas Foster",
      image: "/bananas-foster.jpg",
      recipe: `1. Melt butter and add brown sugar.
2. Stir in cinnamon, banana liqueur, and rum.
3. Add sliced bananas and cook briefly.
4. Flambé and serve over vanilla ice cream.`
    },
    {
      name: "Jambalaya",
      image: "/jambalaya.png",
      recipe: `1. Cook sausage, then add chicken.
2. Add onions, peppers, celery, and garlic.
3. Stir in tomatoes, rice, broth, and spices.
4. Simmer until rice is cooked.
5. Optional: Add shrimp near the end.`
    },
    {
      name: "Boiled Crawfish with Corn and Potatoes",
      image: "/boiled-crawfish.png",
      recipe: `Serves about four people and takes about an hour to make
Ingredients:
12 - 15 pounds live crawfish
8 quarts water
1 package (16 ounces) Zatarain's® Preseasoned Crab Boil
1 large onion, peeled
1 head garlic, halved crosswise
1 1/2 pounds small red potatoes
6 ears corn, shucked and halved crosswise or 12 frozen mini corn-on-the-cob

Cooking Instructions:
1. Pour live crawfish into a washtub or ice chest; cover with water. Wait about a beer as purging takes time. Drain. Repeat 3 to 4 times until crawfish are clean and you are laughing uncontrollably. Drain. Discard any dead crawfish and debris.
2. Mix 8 quarts water, Crab Boil, onion and garlic in large (20-quart) stockpot. Bring to boil on high heat; boil 5 minutes. Add potatoes; boil 5 minutes. Add crawfish and corn; return to boil. Cover and cook 2 minutes.
3. Turn off heat and let stand 20 minutes. Add about 6 to 8 cups of ice to stockpot; let stand 20 minutes to cool. Drain and serve.`
    },
    {
      name: "Turtle Soup",
      image: "/turtle-soup.png",
      recipe: `1. Make a dark roux with butter and flour.
2. Add mirepoix, garlic, and turtle meat.
3. Stir in stock, tomatoes, and seasonings.
4. Simmer until thickened.
5. Add sherry and garnish with egg and parsley.`
    },
    {
      name: "Crawfish Etouffee",
      image: "/crawfish-etouffee.png",
      recipe: `1. Make a roux and add onion, celery, and bell pepper.
2. Stir in garlic, stock, and seasonings.
3. Add crawfish tails and simmer.
4. Serve over rice.`
    },
    {
        name: "Soft shell Crab Poboy",
        image: "/soft-shell-poboy.png",
        recipe: `Ingredients:
Good French bread
Soft-shell crab, cleaned
Shredded lettuce
Sliced tomato
Dill pickle chips
Mayonnaise
Favorite hot sauce
Cooking Instructions:

1. Cook crab - fry or saute.
2. Slice French bread, po-boy style.
3. Slather mayonnaise on each slice.
4. Put the crab on the bread.
5. Dress with lettuce, tomato, pickles and hot sauce.
`

    } ,
    {
        name: "Galatoires Goute and Oysters en Brochette",
        image: "/galatoire-goute.png",
        recipe: `Cooking Instructions (easiest):
Go to Galatoire's and order Galatoire's Goute and Oysters en Brochette
Galatoire's Goute: crabmeat maison, crawfish maison, shrimp remoulade
Oysters en Brochette: fried oysters, bacon, meunière butter

Galatoire's Crawfish Maison

Ingredients:

2 large egg yolks
2 tablespoons red wine vinegar
1 tablespoon Creole mustard or any course, grainy brown mustard
1 teaspoon fresh lemon juice
1 cup vegetable oil
1/4 cup nonpareil capers, drained
1/4 cup chopped scallions (green and white parts)
1 tablespoon chopped curly parsley
salt and freshly ground white pepper to taste
1 pound jumbo lump crawfish
1 small head of iceberg lettuce, washed, dried, and cut into thin ribbons
2 medium vine-ripened tomatoes, cored and cut into six 1-inch-thick slices

Cooking Instructions:
1. Combine the egg yolks, vinegar, mustard, and lemon juice in a food processor and process for 2 minutes. 
2. With the processor running, add the oil slowly in a thin stream and process until emulsified.

Remove to a mixing bowl and gently fold in the capers, scallions, and parsley. Season with salt and white pepper. Chill for 2 to 4 hours. Just before serving, gently fold in the crawfish, taking care not to break up the lumps. Divide the lettuce among 6 servings and top with a slice of tomato. Spoon the crawfish on top of the tomato and serve.
 
Galatoire's Oysters en Brochette

Ingredients:
1 quart Vegetable Oil
12 thick cut slices smoked Bacon, cut in half
36 large shucked Oysters
2 large Eggs
2 cups whole Milk
2 cups All-purpose Flour
2 cups Meuniére Sauce, recipe to follow
6 Toast Points
6 Lemon Wedges

Cooking Instructions:
1. Heat the oil to 350℉ in a large sauté pan. In a separate, medium sauté pan, cook the bacon over medium heat for 3 to 4 minutes. Drain on paper towels. 
2. To assemble the brochettes, skewer 1 piece of bacon then 2 oysters. Repeat twice and end with an additional piece of bacon for a total of 4 pieces of bacon and 6 oysters. Repeat for 5 more skewers.
3. In a medium bowl, whisk together eggs and milk. Dip the skewers into the egg wash. Allow excess to drip off.
4. Place brochettes in flour and coat heavily. Shake off excess and place into the hot oil.
5. Fry 4 to 5 minutes, until golden brown. Drain on paper towels.
6. Slide Oysters off of the skewers into the centers of 6 appetizer plates. 
7. Ladle meuniére sauce over oysters. Garnish with a toast point and lemon wedge.

Meuniére Sauce

1 pound Butter
1 tablespoon fresh Lemon Juice
1 tablespoon Red Wine Vinegar

Cooking Instructions:
1. In a medium saucepan over medium heat, melt the butter, whisking constantly for 8 to 10 minutes, until the sediment in the butter turns dark brown, almost (but not quite) to the point of burning, and the liquid is a deep golden color. 
2. Remove the pan from heat and continue to whisk slowly, adding the lemon juice and the vinegar to the browned butter.
3. The sauce will froth until the acids have evaporated. When the frothing subsides, the sauce is complete.
`}
  ];

  let selected = dishes[0];
  let recipeOpen = true;
  let navOpen = false;
</script>

<style>
  .container {
    max-width: 960px;
    margin: auto;
    padding: 2rem;
    background: linear-gradient(135deg, #fdfcfb 0%, #e2d1c3 100%);
    border-radius: 1rem;
    box-shadow: 0 8px 20px rgba(0, 0, 0, 0.1);
  }
  .mobile-nav-toggle {
    display: none;
    justify-content: flex-end;
    margin-bottom: 1rem;
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
  .mobile-tabs {
    flex-direction: column;
    overflow: hidden;
    transition: max-height 0.4s ease, opacity 0.3s ease;
  }
  .mobile-tabs.open {
    max-height: 500px;
    opacity: 1;
  }
  .tab {
    white-space: nowrap;
    padding: 0.75rem 1.25rem;
    border-radius: 9999px;
    background-color: #f4f4f5;
    color: #333;
    cursor: pointer;
    transition: all 0.3s ease;
    scroll-snap-align: start;
    box-shadow: 0 2px 5px rgba(0,0,0,0.05);
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
  .recipe-img {
    max-width: 100%;
    border-radius: 1.5rem;
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.1);
    margin-bottom: 1.5rem;
    -ms-interpolation-mode: bicubic;
    vertical-align: bottom;
    justify-content: center;
    align-items: center;
  }
  pre {
    white-space: pre-wrap;
    font-family: 'Courier New', monospace;
    background-color: #fff7ed;
    padding: 1.25rem;
    border-left: 4px solid #147A19;
    border-radius: 0.5rem;
    box-shadow: inset 0 1px 3px rgba(0,0,0,0.05);
    overflow-x: auto;
  }
  .accordion {
    border: none;
    border-radius: 0.75rem;
    margin-top: 1rem;
    background: #fff;
    box-shadow: 0 4px 15px rgba(0, 0, 0, 0.07);
    overflow: hidden;
  }
  .accordion-header {
    background: #fcd34d;
    padding: 0.75rem 1.25rem;
    cursor: pointer;
    font-weight: bold;
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: #4b5563;
  }
  .accordion-header:hover {
    background: #fbbf24;
  }


  @media (max-width: 768px) {
    .container {
      padding: 1rem;
      border-radius: 0.75rem;
    }
    .mobile-nav-toggle {
      display: flex;
    }
    .tabs {
      display: none;
    }
    .mobile-tabs {
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
<svelte:head>
	<title>Eat thru New Orleans</title>
</svelte:head>

<div class="container">

  <h1 class="text-5xl font-extrabold mb-4 text-center text-rose-800 drop-shadow" style="display:inline-block;">
    How To Eat Your Way Through</h1><img src="new-orleans-tile.png" alt="New Orleans"/>

  <!-- <div class="mobile-nav-toggle">
    <button onclick={() => navOpen = !navOpen} aria-label="Toggle Navigation">
      <Menu />
    </button>
  </div> -->
<h2>New Orleans is the number ONE food city in the world according to 
    <a href="https://www.timeout.com/travel/worlds-best-cities-for-food">these guys</a></h2>
  <div class="tabs">
    {#each dishes as dish}
      <div
        class="tab {selected.name === dish.name ? 'active' : ''}"
        onclick={() => { selected = dish; recipeOpen = true; }}>
        {dish.name}
      </div>
    {/each}
  </div>
<!-- 
  <div class="mobile-tabs {navOpen ? 'open' : ''}">
    {#each dishes as dish}
      <div
        class="tab {selected.name === dish.name ? 'active' : ''}"
        onclick={() => { selected = dish; recipeOpen = false; navOpen = false; }}>
        {dish.name}
      </div>
    {/each}
  </div> -->

  <div>
    <h2 class="text-3xl font-semibold mb-3 text-gray-800">{selected.name}</h2>
    <img src={selected.image} class="recipe-img" alt={selected.name} />
    <div class="accordion">

        <div in:slide out:slide>
          <div class="accordion-body open">
            <pre>{selected.recipe}</pre>
          </div>
        </div>
    </div>
  </div>
</div>
